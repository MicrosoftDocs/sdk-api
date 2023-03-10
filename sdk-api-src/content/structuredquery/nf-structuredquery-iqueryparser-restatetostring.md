---
UID: NF:structuredquery.IQueryParser.RestateToString
title: IQueryParser::RestateToString (structuredquery.h)
description: Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used.
helpviewer_keywords: ["IQueryParser interface [search]","RestateToString method","IQueryParser.RestateToString","IQueryParser::RestateToString","RestateToString","RestateToString method [search]","RestateToString method [search]","IQueryParser interface","_search_IQueryParser_RestateToString","search._search_IQueryParser_RestateToString","structuredquery/IQueryParser::RestateToString"]
old-location: search\_search_IQueryParser_RestateToString.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\restatetostring.htm
ms.date: 12/05/2018
ms.keywords: IQueryParser interface [search],RestateToString method, IQueryParser.RestateToString, IQueryParser::RestateToString, RestateToString, RestateToString method [search], RestateToString method [search],IQueryParser interface, _search_IQueryParser_RestateToString, search._search_IQueryParser_RestateToString, structuredquery/IQueryParser::RestateToString
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
 - IQueryParser::RestateToString
 - structuredquery/IQueryParser::RestateToString
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
 - IQueryParser.RestateToString
---

# IQueryParser::RestateToString


## -description

Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used.

## -parameters

### -param pCondition [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>*</b>

The condition to be restated.

### -param fUseEnglish [in]

Type: <b>BOOL</b>

Reserved. Must be <b>FALSE</b>.

### -param ppszQueryString [out]

Type: <b>LPWSTR*</b>

Receives the restated query string. The caller must free the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.