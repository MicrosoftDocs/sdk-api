---
UID: NF:searchapi.ISearchLanguageSupport.IsPrefixNormalized
title: ISearchLanguageSupport::IsPrefixNormalized (searchapi.h)
description: Determines whether the query token is a prefix of the document token, disregarding case, width, and (optionally) diacritics.
helpviewer_keywords: ["ISearchLanguageSupport interface [search]","IsPrefixNormalized method","ISearchLanguageSupport.IsPrefixNormalized","ISearchLanguageSupport::IsPrefixNormalized","IsPrefixNormalized","IsPrefixNormalized method [search]","IsPrefixNormalized method [search]","ISearchLanguageSupport interface","_search_ISearchLanguageSupport_IsPrefixNormalized","search._search_ISearchLanguageSupport_IsPrefixNormalized","searchapi/ISearchLanguageSupport::IsPrefixNormalized"]
old-location: search\_search_ISearchLanguageSupport_IsPrefixNormalized.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\isprefixnormalized.htm
ms.date: 12/05/2018
ms.keywords: ISearchLanguageSupport interface [search],IsPrefixNormalized method, ISearchLanguageSupport.IsPrefixNormalized, ISearchLanguageSupport::IsPrefixNormalized, IsPrefixNormalized, IsPrefixNormalized method [search], IsPrefixNormalized method [search],ISearchLanguageSupport interface, _search_ISearchLanguageSupport_IsPrefixNormalized, search._search_ISearchLanguageSupport_IsPrefixNormalized, searchapi/ISearchLanguageSupport::IsPrefixNormalized
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchlanguagesupport.idl
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
 - ISearchLanguageSupport::IsPrefixNormalized
 - searchapi/ISearchLanguageSupport::IsPrefixNormalized
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchLanguageSupport.IsPrefixNormalized
---

# ISearchLanguageSupport::IsPrefixNormalized


## -description

Determines whether the query token is a prefix of the document token, disregarding case, width, and (optionally) diacritics.

## -parameters

### -param pwcsQueryToken [in]

Type: <b>LPCWSTR</b>

Pointer to the prefix to search for.

### -param cwcQueryToken [in]

Type: <b>ULONG</b>

The size of <i>pwcsQueryToken</i>.

### -param pwcsDocumentToken [in]

Type: <b>LPCWSTR</b>

Pointer to the document to be searched.

### -param cwcDocumentToken [in]

Type: <b>ULONG</b>

The size of <i>pwcsDocumentToken</i>.

### -param pulPrefixLength [out]

Type: <b>ULONG*</b>

Returns a pointer to the number of characters matched in <i>pwcsDocumentToken</i>. Typically, but not necessarily, the number of characters in <i>pwcsQueryToken</i>.

## -returns

Type: <b>HRESULT</b>

If <i>pwcsQueryToken</i> is a prefix of <i>pwcsDocumentToken</i>, returns S_OK; otherwise returns S_FALSE, and <i>pulPrefixLength</i> is set to zero.

