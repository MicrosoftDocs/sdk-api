---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



