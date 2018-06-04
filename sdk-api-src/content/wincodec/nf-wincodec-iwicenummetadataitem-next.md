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

# IWICEnumMetadataItem::Next


## -description


Advanced the current position in the enumeration.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of items to be retrieved.


### -param rgeltSchema [in, out]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>

An array of enumerated items. This parameter is optional.


### -param rgeltId [in, out]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>

An array of enumerated items.


### -param rgeltValue [in, out, optional]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>

An array of enumerated items. This parameter is optional.


### -param pceltFetched [out, optional]

Type: <b>ULONG*</b>

The number of items that were retrieved. This value is always less than or equal to the number of items requested.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



