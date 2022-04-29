# request

url = "https://foobar.atlassian.net/wiki/rest/api/content/1147126"

payload = json.dumps(

{"id":1147126,
"type":"page",
"title":"My page 8", 
"ancestors":[{"id":1378762}], 
"space":{"key":"CD"},
"version":{"number":4}})

headers = {
"Accept": "application/json",
"Content-Type": "application/json"
}

r = requests.request("PUT", url, data=payload, headers=headers, auth=auth)

print(r.ok , r.status_code , r.reason, r.url)

jl = json.loads(r.text)
jl
curl -X PUT -H "Authorization: ..." -H "Content-Type: application/json" -d '{"id":1234567,"type":"page", "title":"Your page Title", "ancestors":[{"id":9876543}], "space":{"key":"xxx"},"version":{"number":17}}' "https://abc.def.domain.com/rest/api/content/1234567"





url = "https://foobar.atlassian.net/wiki/rest/api/content/1147126"

payload = json.dumps(

{"id":1147126,
"type":"page",
"title":"My page 8", 
"ancestors":[{"id":1378762}], 
"space":{"key":"CD"},
"version":{"number":4}})

headers = {
"Accept": "application/json",
"Content-Type": "application/json"
}

r = requests.request("PUT", url, data=payload, headers=headers, auth=auth)

print(r.ok , r.status_code , r.reason, r.url)

jl = json.loads(r.text)
jl
