# vegeta_load_samples
This repo provide working examples of some basic cases for API load test using Vegeta on various apps

VEGETA for LOAD TEST: https://github.com/tsenart/vegeta

Load Test Command:
vegeta attack -duration=1800s -rate=.01/s -targets=get_top_5_apps.list -output=get_top_5_apps.bin

Plot Analysis Graph for the given output file:
vegeta plot -title=Graph_Title_Name get_top_5_apps.bin > get_top_5_apps.html

Print Basic Report from the output file:
vegeta report get_top_5_apps.bin

Write Json / CSV / GOB response to json file:
cat get_top_5_apps.bin | vegeta encode -to=json > responses.json