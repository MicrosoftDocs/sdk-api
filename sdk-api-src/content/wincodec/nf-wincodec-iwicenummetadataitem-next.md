---
UID: NF:wincodec.IWICEnumMetadataItem.Next
title: IWICEnumMetadataItem::Next
author: windows-sdk-content
description: Advanced the current position in the enumeration.
old-location: wic\_wic_codec_iwicenummetadataitem_next.htm
tech.root: wic
ms.assetid: e502f42e-573c-416b-9282-dd50827ef132
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICEnumMetadataItem interface [Windows Imaging Component],Next method, IWICEnumMetadataItem.Next, IWICEnumMetadataItem::Next, Next, Next method [Windows Imaging Component], Next method [Windows Imaging Component],IWICEnumMetadataItem interface, _wic_codec_iwicenummetadataitem_next, wic._wic_codec_iwicenummetadataitem_next, wincodec/IWICEnumMetadataItem::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICEnumMetadataItem.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICEnumMetadataItem.Next
: 
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



