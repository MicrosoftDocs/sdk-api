---
UID: NE:mfapi._MFVideo3DFormat
title: MFVideo3DFormat (mfapi.h)
description: Specifies how 3D video frames are stored in memory.
helpviewer_keywords: ["MFVideo3DFormat","MFVideo3DFormat enumeration [Media Foundation]","MFVideo3DSampleFormat_BaseView","MFVideo3DSampleFormat_MultiView","MFVideo3DSampleFormat_Packed_LeftRight","MFVideo3DSampleFormat_Packed_TopBottom","mf.mfvideo3dformat","mfapi/MFVideo3DFormat","mfapi/MFVideo3DSampleFormat_BaseView","mfapi/MFVideo3DSampleFormat_MultiView","mfapi/MFVideo3DSampleFormat_Packed_LeftRight","mfapi/MFVideo3DSampleFormat_Packed_TopBottom"]
old-location: mf\mfvideo3dformat.htm
tech.root: mf
ms.assetid: 0E31BC98-E69D-405E-9EA6-026916123091
ms.date: 12/05/2018
ms.keywords: MFVideo3DFormat, MFVideo3DFormat enumeration [Media Foundation], MFVideo3DSampleFormat_BaseView, MFVideo3DSampleFormat_MultiView, MFVideo3DSampleFormat_Packed_LeftRight, MFVideo3DSampleFormat_Packed_TopBottom, mf.mfvideo3dformat, mfapi/MFVideo3DFormat, mfapi/MFVideo3DSampleFormat_BaseView, mfapi/MFVideo3DSampleFormat_MultiView, mfapi/MFVideo3DSampleFormat_Packed_LeftRight, mfapi/MFVideo3DSampleFormat_Packed_TopBottom
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
req.typenames: MFVideo3DFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideo3DFormat
 - mfapi/_MFVideo3DFormat
 - MFVideo3DFormat
 - mfapi/MFVideo3DFormat
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
 - MFVideo3DFormat
---

# MFVideo3DFormat enumeration


## -description

Specifies how 3D video frames are stored in memory.

## -enum-fields

### -field MFVideo3DSampleFormat_BaseView:0

The base view is stored in a single buffer. The other view is discarded.

### -field MFVideo3DSampleFormat_MultiView:1

Each media sample contains multiple buffers, one for each view.

### -field MFVideo3DSampleFormat_Packed_LeftRight:2

Each media sample contains one buffer, with both views packed side-by-side into a single frame.

### -field MFVideo3DSampleFormat_Packed_TopBottom:3

Each media sample contains one buffer, with both views packed top-and-bottom into a single frame.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-mt-video-3d-format">MF_MT_VIDEO_3D_FORMAT</a> attribute.

## -see-also

Media Foundation Enumerations
