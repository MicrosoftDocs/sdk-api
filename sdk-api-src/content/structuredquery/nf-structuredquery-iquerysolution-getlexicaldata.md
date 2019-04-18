---
UID: NF:structuredquery.IQuerySolution.GetLexicalData
title: IQuerySolution::GetLexicalData (structuredquery.h)
author: windows-sdk-content
description: Reports the query string, how it was tokenized, and what language code identifier (LCID) and word breaker were used to parse it.
old-location: search\_search_IQuerySolution_GetLexicalData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\getlexicaldata.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLexicalData, GetLexicalData method [search], GetLexicalData method [search],IQuerySolution interface, IQuerySolution interface [search],GetLexicalData method, IQuerySolution.GetLexicalData, IQuerySolution::GetLexicalData, _search_IQuerySolution_GetLexicalData, search._search_IQuerySolution_GetLexicalData, structuredquery/IQuerySolution::GetLexicalData
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQuerySolution.GetLexicalData
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IQuerySolution::GetLexicalData


## -description


Reports the query string, how it was tokenized, and what language code identifier (LCID) and word breaker were used to parse it.
        


## -parameters




### -param ppszInputString [out]

Type: <b>LPWSTR*</b>

Receives the query string. This parameter can be <b>NULL</b>.
            


### -param ppTokens [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231300(v=VS.85).aspx">ITokenCollection</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231300(v=VS.85).aspx">ITokenCollection</a> object that describes how the query was tokenized. This parameter can be <b>NULL</b>.
            


### -param plcid [out]

Type: <b>LCID*</b>

Receives a LCID for the word breaker used for this query. This parameter can be <b>NULL</b>.
            


### -param ppWordBreaker [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>**</b>

Receives a pointer to the word breaker used for this query. This parameter can be <b>NULL</b>.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



