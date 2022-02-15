---
UID: NF:structuredquery.ITokenCollection.GetToken
title: ITokenCollection::GetToken (structuredquery.h)
description: Retrieves the position, length, and any overriding string of an individual token.
helpviewer_keywords: ["GetToken","GetToken method [search]","GetToken method [search]","ITokenCollection interface","ITokenCollection interface [search]","GetToken method","ITokenCollection.GetToken","ITokenCollection::GetToken","_search_ITokenCollection_GetToken","search._search_ITokenCollection_GetToken","structuredquery/ITokenCollection::GetToken"]
old-location: search\_search_ITokenCollection_GetToken.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\itokencollection\gettoken.htm
ms.date: 12/05/2018
ms.keywords: GetToken, GetToken method [search], GetToken method [search],ITokenCollection interface, ITokenCollection interface [search],GetToken method, ITokenCollection.GetToken, ITokenCollection::GetToken, _search_ITokenCollection_GetToken, search._search_ITokenCollection_GetToken, structuredquery/ITokenCollection::GetToken
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
 - ITokenCollection::GetToken
 - structuredquery/ITokenCollection::GetToken
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
 - ITokenCollection.GetToken
---

# ITokenCollection::GetToken


## -description

Retrieves the position, length, and any overriding string of an individual token.

## -parameters

### -param i [in]

Type: <b>ULONG</b>

The zero-based index of the desired token within the collection.

### -param pBegin [out]

Type: <b>ULONG*</b>

Receives the zero-based starting position of the specified token, in characters. This parameter can be <b>NULL</b>.

### -param pLength [out]

Type: <b>ULONG*</b>

Receives the number of characters spanned by the token. This parameter can be <b>NULL</b>.

### -param ppsz [out]

Type: <b>LPWSTR*</b>

Receives the overriding text for this token if available, or <b>NULL</b> if there is none.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

