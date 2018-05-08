---
UID: NF:searchapi.ISearchLanguageSupport.IsPrefixNormalized
title: ISearchLanguageSupport::IsPrefixNormalized
author: windows-driver-content
description: Determines whether the query token is a prefix of the document token, disregarding case, width, and (optionally) diacritics.
old-location: search\_search_ISearchLanguageSupport_IsPrefixNormalized.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\isprefixnormalized.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ISearchLanguageSupport interface [search],IsPrefixNormalized method, ISearchLanguageSupport.IsPrefixNormalized, ISearchLanguageSupport::IsPrefixNormalized, IsPrefixNormalized, IsPrefixNormalized method [search], IsPrefixNormalized method [search],ISearchLanguageSupport interface, _search_ISearchLanguageSupport_IsPrefixNormalized, search._search_ISearchLanguageSupport_IsPrefixNormalized, searchapi/ISearchLanguageSupport::IsPrefixNormalized
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchLanguageSupport.IsPrefixNormalized
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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



