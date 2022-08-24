import requests
import json


vulnurl = "https://AgraphQLURL/"
payloadFile = open(r"introspectionquery", "r+")

GQLpayload = payloadFile.read()

GQLjsonPayload = json.loads(GQLpayload)


def NographisSafe(url):
    Graphdata = requests.post(url, json=GQLjsonPayload)

    GraphSchema = Graphdata.content

    return GraphSchema


print(NographisSafe(vulnurl))
