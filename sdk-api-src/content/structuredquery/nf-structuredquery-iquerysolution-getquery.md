---
UID: NF:structuredquery.IQuerySolution.GetQuery
title: IQuerySolution::GetQuery (structuredquery.h)
description: Retrieves the condition tree and the semantic type of the solution.
helpviewer_keywords: ["GetQuery","GetQuery method [search]","GetQuery method [search]","IQuerySolution interface","IQuerySolution interface [search]","GetQuery method","IQuerySolution.GetQuery","IQuerySolution::GetQuery","_search_IQuerySolution_GetQuery","search._search_IQuerySolution_GetQuery","structuredquery/IQuerySolution::GetQuery"]
old-location: search\_search_IQuerySolution_GetQuery.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\getquery.htm
ms.date: 12/05/2018
ms.keywords: GetQuery, GetQuery method [search], GetQuery method [search],IQuerySolution interface, IQuerySolution interface [search],GetQuery method, IQuerySolution.GetQuery, IQuerySolution::GetQuery, _search_IQuerySolution_GetQuery, search._search_IQuerySolution_GetQuery, structuredquery/IQuerySolution::GetQuery
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
 - IQuerySolution::GetQuery
 - structuredquery/IQuerySolution::GetQuery
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
 - IQuerySolution.GetQuery
---

# IQuerySolution::GetQuery


## -description

Retrieves the condition tree and the semantic type of the solution.

## -parameters

### -param ppQueryNode [out]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> condition tree that is the interpretation of the query string. This parameter can be <b>NULL</b>.

### -param ppMainType [out]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a> object that identifies the semantic type of the interpretation. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.