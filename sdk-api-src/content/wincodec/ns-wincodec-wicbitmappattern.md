---
UID: NS:wincodec.WICBitmapPattern
title: WICBitmapPattern
author: windows-sdk-content
description: Contains members that identify a pattern within an image file which can be used to identify a particular format.
old-location: wic\_wic_codec_wicbitmappattern.htm
old-project: wic
ms.assetid: 6f0cd639-c0db-46e4-b3a3-bc21222d97ee
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: WICBitmapPattern, WICBitmapPattern structure [Windows Imaging Component], _wic_codec_wicbitmappattern, wic._wic_codec_wicbitmappattern, wincodec/WICBitmapPattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WICBitmapPattern
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICBitmapPattern structure


## -description


Contains members that identify a pattern within an image file which can be used to identify a particular format.


## -struct-fields




### -field Position

Type: <b>ULARGE_INTEGER</b>

The offset the pattern is located in the file.


### -field Length

Type: <b>ULONG</b>

The pattern length.


### -field Pattern

Type: <b>BYTE*</b>

The actual pattern.


### -field Mask

Type: <b>BYTE*</b>

The pattern mask.


### -field EndOfStream

Type: <b>BOOL</b>

The end of the stream.

