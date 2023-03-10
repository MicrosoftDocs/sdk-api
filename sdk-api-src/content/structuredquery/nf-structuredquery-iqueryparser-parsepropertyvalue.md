---
UID: NF:structuredquery.IQueryParser.ParsePropertyValue
title: IQueryParser::ParsePropertyValue (structuredquery.h)
description: Parses a condition for a specified property.
helpviewer_keywords: ["IQueryParser interface [search]","ParsePropertyValue method","IQueryParser.ParsePropertyValue","IQueryParser::ParsePropertyValue","ParsePropertyValue","ParsePropertyValue method [search]","ParsePropertyValue method [search]","IQueryParser interface","_search_IQueryParser_ParsePropertyValue","search._search_IQueryParser_ParsePropertyValue","structuredquery/IQueryParser::ParsePropertyValue"]
old-location: search\_search_IQueryParser_ParsePropertyValue.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\parsepropertyvalue.htm
ms.date: 12/05/2018
ms.keywords: IQueryParser interface [search],ParsePropertyValue method, IQueryParser.ParsePropertyValue, IQueryParser::ParsePropertyValue, ParsePropertyValue, ParsePropertyValue method [search], ParsePropertyValue method [search],IQueryParser interface, _search_IQueryParser_ParsePropertyValue, search._search_IQueryParser_ParsePropertyValue, structuredquery/IQueryParser::ParsePropertyValue
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IQueryParser::ParsePropertyValue
 - structuredquery/IQueryParser::ParsePropertyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQueryParser.ParsePropertyValue
---

# IQueryParser::ParsePropertyValue


## -description

Parses a condition for a specified property.

## -parameters

### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Property name.

### -param pszInputString [in]

Type: <b>LPCWSTR</b>

Query string to be parsed, relative to that property.

### -param ppSolution [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a>**</b>

Receives an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> object. The calling application must release it by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The input string can be anything that could have been written immediately after a property in a structured query. For example, "from:(bill OR alex)" would be a valid structured query, so passing System.StructuredQuery.Virtual.From (for which From is a keyword) in the <i>pszPropertyName</i> parameter and "(bill OR alex)" or "bill OR alex" in the <i>pszInputString</i> parameter would be valid. This would result in an <b>OR</b> of leaf nodes that relate the System.StructuredQuery.Virtual.From property with the strings "bill" and "alex".