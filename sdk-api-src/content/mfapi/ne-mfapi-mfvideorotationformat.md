---
UID: NE:mfapi._MFVideoRotationFormat
title: MFVideoRotationFormat (mfapi.h)
description: Describes the rotation of the video image in the counter-clockwise direction.
helpviewer_keywords: ["MFVideoRotationFormat","MFVideoRotationFormat enumeration [Media Foundation]","MFVideoRotationFormat_0","MFVideoRotationFormat_180","MFVideoRotationFormat_270","MFVideoRotationFormat_90","mf.mfvideorotationformat","mfapi/MFVideoRotationFormat","mfapi/MFVideoRotationFormat_0","mfapi/MFVideoRotationFormat_180","mfapi/MFVideoRotationFormat_270","mfapi/MFVideoRotationFormat_90"]
old-location: mf\mfvideorotationformat.htm
tech.root: mf
ms.assetid: E2760742-3914-4B5C-87FB-38F2EF3025C3
ms.date: 12/05/2018
ms.keywords: MFVideoRotationFormat, MFVideoRotationFormat enumeration [Media Foundation], MFVideoRotationFormat_0, MFVideoRotationFormat_180, MFVideoRotationFormat_270, MFVideoRotationFormat_90, mf.mfvideorotationformat, mfapi/MFVideoRotationFormat, mfapi/MFVideoRotationFormat_0, mfapi/MFVideoRotationFormat_180, mfapi/MFVideoRotationFormat_270, mfapi/MFVideoRotationFormat_90
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MFVideoRotationFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoRotationFormat
 - mfapi/_MFVideoRotationFormat
 - MFVideoRotationFormat
 - mfapi/MFVideoRotationFormat
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
 - MFVideoRotationFormat
---

# MFVideoRotationFormat enumeration


## -description

Describes the rotation of the video image in the counter-clockwise direction.

## -enum-fields

### -field MFVideoRotationFormat_0:0

The image is not rotated.

### -field MFVideoRotationFormat_90:90

The image is rotated 90 degrees counter-clockwise.

### -field MFVideoRotationFormat_180:180

The image is rotated 180 degrees.

### -field MFVideoRotationFormat_270:270

The image is rotated 270 degrees counter-clockwise.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-mt-video-rotation">MF_MT_VIDEO_ROTATION</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
