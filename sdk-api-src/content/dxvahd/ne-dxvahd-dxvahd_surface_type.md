---
UID: NE:dxvahd._DXVAHD_SURFACE_TYPE
title: DXVAHD_SURFACE_TYPE (dxvahd.h)
description: Specifies the type of video surface created by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_SURFACE_TYPE","DXVAHD_SURFACE_TYPE enumeration [Media Foundation]","DXVAHD_SURFACE_TYPE_VIDEO_INPUT","DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE","DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT","dxvahd/DXVAHD_SURFACE_TYPE","dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_INPUT","dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE","dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT","mf.dxvahd_surface_type"]
old-location: mf\dxvahd_surface_type.htm
tech.root: mf
ms.assetid: 06df2d2f-9163-4672-8ea4-57f1942320c5
ms.date: 12/05/2018
ms.keywords: DXVAHD_SURFACE_TYPE, DXVAHD_SURFACE_TYPE enumeration [Media Foundation], DXVAHD_SURFACE_TYPE_VIDEO_INPUT, DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE, DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT, dxvahd/DXVAHD_SURFACE_TYPE, dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_INPUT, dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE, dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT, mf.dxvahd_surface_type
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_SURFACE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_SURFACE_TYPE
 - dxvahd/_DXVAHD_SURFACE_TYPE
 - DXVAHD_SURFACE_TYPE
 - dxvahd/DXVAHD_SURFACE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_SURFACE_TYPE
---

# DXVAHD_SURFACE_TYPE enumeration


## -description

Specifies the type of video surface created by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -enum-fields

### -field DXVAHD_SURFACE_TYPE_VIDEO_INPUT:0

A surface for an input stream. This surface type is equivalent to an off-screen plain surface in Microsoft Direct3D. The application can use the surface in Direct3D calls.

### -field DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE:1

A private surface for an input stream. This surface type is equivalent to an off-screen plain surface, except that the application cannot use the surface in Direct3D calls.

### -field DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT:2

A surface for an output stream. This surface type is equivalent to an off-screen plain surface in Direct3D. The application can use the surface in Direct3D calls. 

This surface type is recommended for video processing applications that need to lock the surface and access the surface memory. For video playback with optimal performance, a render-target surface or swap chain is recommended instead.

## -remarks

If the DXVA-HD device is a software plug-in and the surface type is <b>DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE</b>, the device can support format types that are not supported natively by the graphics driver. For example, if the application requests an AYUV surface, the device could allocate a surface with a surface type of <b>D3DFMT_A8R8G8B8</b>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">IDXVAHD_Device::CreateVideoSurface</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
