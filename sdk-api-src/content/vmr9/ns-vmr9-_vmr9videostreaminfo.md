---
UID: NS:vmr9._VMR9VideoStreamInfo
title: "_VMR9VideoStreamInfo"
author: windows-sdk-content
description: The VMR9VideoStreamInfo structure describes the rendering parameters for a video compositing operation in the VRM-9 filter. This structure is used in the IVMRImageCompositor9::CompositeImage method.
old-location: dshow\vmr9videostreaminfo.htm
old-project: DirectShow
ms.assetid: e2da0c1e-d592-49ce-937c-0d75ce270282
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: VMR9VideoStreamInfo, VMR9VideoStreamInfo structure [DirectShow], VMR9VideoStreamInfoStructure, _VMR9VideoStreamInfo, dshow.vmr9videostreaminfo, vmr9/VMR9VideoStreamInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: VMR9VideoStreamInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9VideoStreamInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VMR9VideoStreamInfo structure


## -description



The <code>VMR9VideoStreamInfo</code> structure describes the rendering parameters for a video compositing operation in the VRM-9 filter. This structure is used in the <a href="https://msdn.microsoft.com/a59d21e8-faa2-484d-9d82-991c6bc4e045">IVMRImageCompositor9::CompositeImage</a> method.




## -struct-fields




### -field pddsVideoSurface

A pointer to the <a href="https://msdn.microsoft.com/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a> interface of the Direct3D surface that contains the video to be composited.


### -field dwWidth

The width of the video rectangle.
          


### -field dwHeight

The height of the video rectangle.
          


### -field dwStrmID

Specifies the input stream. This value corresponds to the input pin.


### -field fAlpha

The alpha value for this stream. (Not per-pixel alpha.)
          


### -field rNormal

The position of the image in composition space, as a <a href="https://msdn.microsoft.com/226b685c-92da-45c3-b99a-6c1e732f8dc6">VMR9NormalizedRect</a> structure.
          


### -field rtStart

The start time of the video frame, in 100-nanosecond units.


### -field rtEnd

The end time of the video frame, in 100-nanosecond units.


### -field SampleFormat

The video interlacing format, specified as a member of the <a href="https://msdn.microsoft.com/0e501c05-91ac-4594-bdfe-e8b4bfeb5bcb">VMR9_SampleFormat</a> enumeration type.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

