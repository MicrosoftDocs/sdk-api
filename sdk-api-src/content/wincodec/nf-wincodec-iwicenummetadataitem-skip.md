---
UID: NF:wincodec.IWICEnumMetadataItem.Skip
title: IWICEnumMetadataItem::Skip
author: windows-driver-content
description: Skips to given number of objects.
old-location: wic\_wic_codec_iwicenummetadataitem_skip.htm
old-project: wic
ms.assetid: 05c1c69c-ad87-42ff-947d-1f39a70605f3
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICEnumMetadataItem interface [Windows Imaging Component],Skip method, IWICEnumMetadataItem.Skip, IWICEnumMetadataItem::Skip, Skip, Skip method [Windows Imaging Component], Skip method [Windows Imaging Component],IWICEnumMetadataItem interface, _wic_codec_iwicenummetadataitem_skip, wic._wic_codec_iwicenummetadataitem_skip, wincodec/IWICEnumMetadataItem::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICEnumMetadataItem.Skip
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICEnumMetadataItem::Skip


## -description


Skips to given number of objects.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of objects to skip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



