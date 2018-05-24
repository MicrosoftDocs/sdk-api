---
UID: NF:structuredquery.IQueryParser.RestateToString
title: IQueryParser::RestateToString
author: windows-driver-content
description: Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used.
old-location: search\_search_IQueryParser_RestateToString.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\restatetostring.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IQueryParser interface [search],RestateToString method, IQueryParser.RestateToString, IQueryParser::RestateToString, RestateToString, RestateToString method [search], RestateToString method [search],IQueryParser interface, _search_IQueryParser_RestateToString, search._search_IQueryParser_RestateToString, structuredquery/IQueryParser::RestateToString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IQueryParser.RestateToString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQueryParser::RestateToString


## -description


Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used.


## -parameters




### -param pCondition [in]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>*</b>

The condition to be restated.


### -param fUseEnglish [in]

Type: <b>BOOL</b>

Reserved. Must be <b>FALSE</b>.


### -param ppszQueryString [out]

Type: <b>LPWSTR*</b>

Receives the restated query string. The caller must free the string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



