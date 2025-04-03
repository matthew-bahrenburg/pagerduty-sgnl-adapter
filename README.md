# Pager Duty SGNL Adapter

The SGNL Adapter used for collecting PagerDuty Teams data: https://api.pagerduty.com/teams

## To Run

- Clone this repo: `git clone https://github.com/matthew-bahrenburg/pagerduty-sgnl-adapter` 
- Change into the new directory: `cd pagerduty-sgnl-adapter`
- Create a JSON file (for example, authTokens.json) that will contain the tokens used to authenticate requests to the adapter. The tokens must be stored in the following format and note down the path of the file. Auth tokens can be generated using `openssl rand 64 | openssl enc -base64 -A`
   ```
   ["<token1>", "<token2>", ...]
   ```
- Get the path to the authtokens.json file by running: `ls `pwd`/authTokens.json`
- Set environment variable AUTH_TOKENS_PATH `export AUTH_TOKENS_PATH=<PATH TO authtokens.json file>`
- In the pagerduty-sgnl-adapter directory, execute the following command to start the adapter running locally on port 8080 `go run cmd/adapter/main.go`

For more information, see https://help.sgnl.ai/articles/systems-of-record/creating-and-configuring-custom-adapter/
