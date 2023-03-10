---
UID: NE:mfapi._MFFrameSourceTypes
title: MFFrameSourceTypes (mfapi.h)
description: Describes the type of data provided by a frame source.
helpviewer_keywords: ["MFFrameSourceTypes","MFFrameSourceTypes enumeration [Media Foundation]","MFFrameSourceTypes_Color","MFFrameSourceTypes_Custom","MFFrameSourceTypes_Depth","MFFrameSourceTypes_Image","MFFrameSourceTypes_Infrared","_MFFrameSourceTypes","mf.mfframesourcetypes","mfapi/ MFFrameSourceTypes_Image","mfapi/MFFrameSourceTypes","mfapi/MFFrameSourceTypes_Color","mfapi/MFFrameSourceTypes_Custom","mfapi/MFFrameSourceTypes_Depth","mfapi/MFFrameSourceTypes_Infrared"]
old-location: mf\mfframesourcetypes.htm
tech.root: mf
ms.assetid: F5926479-C41D-4702-8220-6A79859BD0F4
ms.date: 12/05/2018
ms.keywords: MFFrameSourceTypes, MFFrameSourceTypes enumeration [Media Foundation], MFFrameSourceTypes_Color, MFFrameSourceTypes_Custom, MFFrameSourceTypes_Depth, MFFrameSourceTypes_Image, MFFrameSourceTypes_Infrared, _MFFrameSourceTypes, mf.mfframesourcetypes, mfapi/ MFFrameSourceTypes_Image, mfapi/MFFrameSourceTypes, mfapi/MFFrameSourceTypes_Color, mfapi/MFFrameSourceTypes_Custom, mfapi/MFFrameSourceTypes_Depth, mfapi/MFFrameSourceTypes_Infrared
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
targetos: Windows
req.typenames: MFFrameSourceTypes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFFrameSourceTypes
 - mfapi/_MFFrameSourceTypes
 - MFFrameSourceTypes
 - mfapi/MFFrameSourceTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFFrameSourceTypes
---

# MFFrameSourceTypes enumeration


## -description

Describes the type of data provided by a frame source.

## -enum-fields

### -field MFFrameSourceTypes_Color:0x0001

The frame source provides color data.

### -field MFFrameSourceTypes_Infrared:0x0002

The frame source provides infrared data.

### -field MFFrameSourceTypes_Depth:0x0004

The frame source provides depth data.

### -field MFFrameSourceTypes_Image:0x0008

The frame source provides image data.

<b>Note</b>  This value was added in Windows 10, version 1803.

### -field MFFrameSourceTypes_Custom:0x0080

The frame source provides custom data.

## -remarks

The values of this enumeration are used with the <a href="/windows/desktop/medfound/mf-devicestream-attribute-framesource-types">MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES</a> attribute.
