---
UID: NF:structuredquery.ITokenCollection.NumberOfTokens
title: ITokenCollection::NumberOfTokens (structuredquery.h)
description: Retrieves the number of tokens in the collection.
helpviewer_keywords: ["ITokenCollection interface [search]","NumberOfTokens method","ITokenCollection.NumberOfTokens","ITokenCollection::NumberOfTokens","NumberOfTokens","NumberOfTokens method [search]","NumberOfTokens method [search]","ITokenCollection interface","_search_ITokenCollection_NumberOfTokens","search._search_ITokenCollection_NumberOfTokens","structuredquery/ITokenCollection::NumberOfTokens"]
old-location: search\_search_ITokenCollection_NumberOfTokens.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\itokencollection\numberoftokens.htm
ms.date: 12/05/2018
ms.keywords: ITokenCollection interface [search],NumberOfTokens method, ITokenCollection.NumberOfTokens, ITokenCollection::NumberOfTokens, NumberOfTokens, NumberOfTokens method [search], NumberOfTokens method [search],ITokenCollection interface, _search_ITokenCollection_NumberOfTokens, search._search_ITokenCollection_NumberOfTokens, structuredquery/ITokenCollection::NumberOfTokens
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
 - ITokenCollection::NumberOfTokens
 - structuredquery/ITokenCollection::NumberOfTokens
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
 - ITokenCollection.NumberOfTokens
---

# ITokenCollection::NumberOfTokens


## -description

Retrieves the number of tokens in the collection.

## -parameters

### -param pCount [out]

Type: <b>ULONG*</b>

Receives the number of tokens within the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

