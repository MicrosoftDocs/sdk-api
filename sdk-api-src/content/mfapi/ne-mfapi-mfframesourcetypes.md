---
UID: NE:mfapi._MFFrameSourceTypes
title: MFFrameSourceTypes (mfapi.h)
author: windows-sdk-content
description: Describes the type of data provided by a frame source.
old-location: mf\mfframesourcetypes.htm
tech.root: medfound
ms.assetid: F5926479-C41D-4702-8220-6A79859BD0F4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFFrameSourceTypes, MFFrameSourceTypes enumeration [Media Foundation], MFFrameSourceTypes_Color, MFFrameSourceTypes_Custom, MFFrameSourceTypes_Depth, MFFrameSourceTypes_Image, MFFrameSourceTypes_Infrared, _MFFrameSourceTypes, mf.mfframesourcetypes, mfapi/ MFFrameSourceTypes_Image, mfapi/MFFrameSourceTypes, mfapi/MFFrameSourceTypes_Color, mfapi/MFFrameSourceTypes_Custom, mfapi/MFFrameSourceTypes_Depth, mfapi/MFFrameSourceTypes_Infrared
ms.topic: enum
f1_keywords: 
 - "mfapi/MFFrameSourceTypes"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFFrameSourceTypes
targetos: Windows
req.typenames: MFFrameSourceTypes
req.redist: 
ms.custom: 19H1
---

# MFFrameSourceTypes enumeration


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

The frame source provides image data.

<b>Note</b>  This value was added in Windows 10, version 1803.


### -field MFFrameSourceTypes_Custom

The frame source provides custom data.


## -remarks



The values of this enumeration are used with the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-devicestream-attribute-framesource-types">MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES</a> attribute.



