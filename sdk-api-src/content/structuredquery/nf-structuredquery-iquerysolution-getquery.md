---
UID: NF:structuredquery.IQuerySolution.GetQuery
title: IQuerySolution::GetQuery
author: windows-sdk-content
description: Retrieves the condition tree and the semantic type of the solution.
old-location: search\_search_IQuerySolution_GetQuery.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\getquery.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetQuery, GetQuery method [search], GetQuery method [search],IQuerySolution interface, IQuerySolution interface [search],GetQuery method, IQuerySolution.GetQuery, IQuerySolution::GetQuery, _search_IQuerySolution_GetQuery, search._search_IQuerySolution_GetQuery, structuredquery/IQuerySolution::GetQuery
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQuerySolution.GetQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQuerySolution::GetQuery


## -description


Retrieves the condition tree and the semantic type of the solution.
        


## -parameters




### -param ppQueryNode [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> condition tree that is the interpretation of the query string. This parameter can be <b>NULL</b>.
            


### -param ppMainType [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231373(v=VS.85).aspx">IEntity</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231373(v=VS.85).aspx">IEntity</a> object that identifies the semantic type of the interpretation. This parameter can be <b>NULL</b>.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



