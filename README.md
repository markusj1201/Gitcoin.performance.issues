# Gitcoin.performance.issues
Audit Gitcoin performance issues

Description
Right now the gitcoin API is unacceptably slow.

kevinowocki@local /Users/kevinowocki~ % time curl "https://gitcoin.co/api/v0.1/bounties/?network=mainnet&idx_status=open&order_by=-web3_created&offset=25&limit=25" > /dev/null
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  288k  100  288k    0     0  66607      0  0:00:04  0:00:04 --:--:-- 71858
curl  > /dev/null  0.02s user 0.02s system 0% cpu 4.449 total
The above request returns 25 results and takes 4.5 seconds. Ideally it should take 1/30th of that amount of time.
