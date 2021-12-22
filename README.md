<div align="center">
  <h1>issueasset</h1>
</div>

<div align="center">  
<i>Web Contract to Issue Assets</i>
</div>

---

<div align="center">
<h4>Documentation</h4>
</div>
  
---
  
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/webcontracts/issueasset/blob/gh-pages/LICENSE)
[![npm](https://img.shields.io/npm/v/webcontract-issueasset)](https://npmjs.com/package/webcontract-issueasset)
[![npm](https://img.shields.io/npm/dw/webcontract-issueasset.svg)](https://npmjs.com/package/webcontract-issueasset)
[![Github Stars](https://img.shields.io/github/stars/webcontracts/issueasset.svg)](https://github.com/webcontracts/issueasset/)
  
# ⚡️ Introduction

issueasset is a web contract to allow you to issue an asset

# Data Model

issueasset allows you to issue new assets

## Asset

Here is a full example of a asset Object

```
{
  "@id": "cuid:a74xt3jbin",
  "amount": 1000000,
  "name": "Melcoin",
  "ticker": "MEL"|,
  "description": "Melcoin tokens",
  "precision": 2,
  "owner": "https://melvincarvalho.com/#me"
}
```

## Location

The issued asset will live in the webcredits directory

## Signing

Currently signing is done out of band using the [gitmark](https://git-mark.com/) protocol, but explicit signing will be added, in future

# ✍️ API

```
issueasset.js <amount> <name> <ticker> <description> <owner>
```

The following switches are allowed
```
--amount      # how much
--name        # the name of the asset
--ticker      # the ticker of the asset
--description # a description of why
--precision   # number of decimal places
--owner       # owner of the asset
```

or from npm 

```JavaScript
import issueasset from 'webcontracts-issueasset'

var asset = {
  amount: data.amount,
  name: data.name,
  ticker: data.ticker,
  description: data.description,
  precision: data.precision,
  owner: data.owner
}

function issueasset(asset, indir, infile)
```

indir and infile are optional and will default to `../webcredits/webcredits.json`


# ⚖️ License

- MIT
