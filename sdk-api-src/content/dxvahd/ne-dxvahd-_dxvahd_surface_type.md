---
UID: NE:dxvahd._DXVAHD_SURFACE_TYPE
title: "_DXVAHD_SURFACE_TYPE"
author: windows-sdk-content
description: Specifies the type of video surface created by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_surface_type.htm
old-project: medfound
ms.assetid: 06df2d2f-9163-4672-8ea4-57f1942320c5
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: DXVAHD_SURFACE_TYPE, DXVAHD_SURFACE_TYPE enumeration [Media Foundation], DXVAHD_SURFACE_TYPE_VIDEO_INPUT, DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE, DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT, _DXVAHD_SURFACE_TYPE, dxvahd/DXVAHD_SURFACE_TYPE, dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_INPUT, dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE, dxvahd/DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT, mf.dxvahd_surface_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DXVAHD_SURFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_SURFACE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_SURFACE_TYPE enumeration


## -description


Specifies the type of video surface created by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -enum-fields




### -field DXVAHD_SURFACE_TYPE_VIDEO_INPUT

A surface for an input stream. This surface type is equivalent to an off-screen plain surface in Microsoft Direct3D. The application can use the surface in Direct3D calls.


### -field DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE

A private surface for an input stream. This surface type is equivalent to an off-screen plain surface, except that the application cannot use the surface in Direct3D calls.


### -field DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT

A surface for an output stream. This surface type is equivalent to an off-screen plain surface in Direct3D. The application can use the surface in Direct3D calls. 

This surface type is recommended for video processing applications that need to lock the surface and access the surface memory. For video playback with optimal performance, a render-target surface or swap chain is recommended instead.


## -remarks



If the DXVA-HD device is a software plug-in and the surface type is <b>DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE</b>, the device can support format types that are not supported natively by the graphics driver. For example, if the application requests an AYUV surface, the device could allocate a surface with a surface type of <b>D3DFMT_A8R8G8B8</b>.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/c467a077-104c-443d-896b-d69441aa5160">IDXVAHD_Device::CreateVideoSurface</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

