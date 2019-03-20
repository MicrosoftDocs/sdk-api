---
UID: NS:amva._tag_AMVAUncompDataInfo
title: AMVAUncompDataInfo (amva.h)
author: windows-sdk-content
description: The AMVAUncompDataInfo structure specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.
old-location: dshow\amvauncompdatainfo.htm
tech.root: DirectShow
ms.assetid: 920f88bb-c671-4ab9-b482-b03505cca118
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPAMVAUncompDataInfo, AMVAUncompDataInfo, AMVAUncompDataInfo structure [DirectShow], AMVAUncompDataInfoStructure, LPAMVAUncompDataInfo, LPAMVAUncompDataInfo structure pointer [DirectShow], amva/AMVAUncompDataInfo, amva/LPAMVAUncompDataInfo, dshow.amvauncompdatainfo"
ms.topic: struct
req.header: amva.h
req.include-header: Videoacc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - amva.h
api_name:
 - AMVAUncompDataInfo
product: Windows
targetos: Windows
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
req.redist: 
---

# AMVAUncompDataInfo structure


## -description


The <b>AMVAUncompDataInfo</b> structure specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.


## -struct-fields




### -field dwUncompWidth

Width of the decoded, uncompressed data, in pixels.


### -field dwUncompHeight

Height of the decoded, uncompressed data, in pixels.
          


### -field ddUncompPixelFormat

A <b>DDPIXELFORMAT</b> structure that specifies the pixel format of the uncompressed data.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376004(v=VS.85).aspx">IAMVideoAccelerator::GetCompBufferInfo</a>
 

 

