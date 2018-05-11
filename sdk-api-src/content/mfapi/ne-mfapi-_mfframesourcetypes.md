---
UID: NE:mfapi._MFFrameSourceTypes
title: "_MFFrameSourceTypes"
author: windows-driver-content
description: Describes the type of data provided by a frame source.
old-location: mf\mfframesourcetypes.htm
old-project: medfound
ms.assetid: F5926479-C41D-4702-8220-6A79859BD0F4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MFFrameSourceTypes, MFFrameSourceTypes enumeration [Media Foundation], MFFrameSourceTypes_Color, MFFrameSourceTypes_Custom, MFFrameSourceTypes_Depth, MFFrameSourceTypes_Image, MFFrameSourceTypes_Infrared, _MFFrameSourceTypes, mf.mfframesourcetypes, mfapi/ MFFrameSourceTypes_Image, mfapi/MFFrameSourceTypes, mfapi/MFFrameSourceTypes_Color, mfapi/MFFrameSourceTypes_Custom, mfapi/MFFrameSourceTypes_Depth, mfapi/MFFrameSourceTypes_Infrared
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFFrameSourceTypes
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	MFFrameSourceTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFFrameSourceTypes enumeration


## -description


Describes the type of data provided by a frame source.


## -enum-fields




### -field MFFrameSourceTypes_Color

The frame source provides color data.


### -field MFFrameSourceTypes_Infrared

The frame source provides infrared data.


### -field MFFrameSourceTypes_Depth

The frame source provides depth data.


### -field MFFrameSourceTypes_Image

<b>Note</b>  This value was added in Windows 10, version 1803.

The frame source provides image data.


### -field MFFrameSourceTypes_Custom

The frame source provides custom data.


## -remarks



The values of this enumeration are used with the <a href="https://msdn.microsoft.com/4A2B427E-E654-48BA-8BF4-16F1B1F8D266">MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES</a> attribute.



