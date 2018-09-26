---
UID: NS:amva._tag_AMVAUncompBufferInfo
title: "_tag_AMVAUncompBufferInfo"
author: windows-sdk-content
description: The AMVAUncompBufferInfo structure describes the uncompressed surfaces to be allocated by the video renderer.
old-location: dshow\amvauncompbufferinfo.htm
tech.root: DirectShow
ms.assetid: 113cc7ba-d05e-48a7-88cb-13645beb16d1
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: "*LPAMVAUncompBufferInfo, AMVAUncompBufferInfo, AMVAUncompBufferInfo structure [DirectShow], AMVAUncompBufferInfoStructure, LPAMVAUncompBufferInfo, LPAMVAUncompBufferInfo structure pointer [DirectShow], _tag_AMVAUncompBufferInfo, amva/AMVAUncompBufferInfo, amva/LPAMVAUncompBufferInfo, dshow.amvauncompbufferinfo"
ms.prod: windows
ms.technology: windows-sdk
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
 - AMVAUncompBufferInfo
product: Windows
targetos: Windows
req.typenames: AMVAUncompBufferInfo, *LPAMVAUncompBufferInfo
req.redist: 
---

# _tag_AMVAUncompBufferInfo structure


## -description


The <b>AMVAUncompBufferInfo</b> structure describes the uncompressed surfaces to be allocated by the video renderer.
          
        


## -struct-fields




### -field dwMinNumSurfaces

Minimum number of surfaces to allocate.
          


### -field dwMaxNumSurfaces

Maximum number of surfaces to allocate.
          


### -field ddUncompPixelFormat

<b>DDPIXELFORMAT</b> structure, describing the pixel format of the allocated surfaces.


## -remarks



The VMR-7 and VMR-9 filters allocate at least <b>dwMinNumSurfaces</b> surfaces. For interlaced content, the VMR-7 allocates additional surfaces equal to the number of forward and backward reference frames required by the deinterlacer. The VMR-7 gets these values by calling <a href="https://msdn.microsoft.com/e672f3d4-1009-4c4c-bb1a-08f78c128423">IVMRDeinterlaceControl::GetDeinterlaceModeCaps</a>. The VMR-9 does not need to allocate additional surfaces for deinterlacing. Thus:

<ul>
<li>For the VMR-7, the number of allocated surfaces is <b>dwMinNumSurfaces</b> + <b>dwNumForwardRefSamples</b> + <b>dwNumBackwardRefSamples</b>. For progressive content, the last two values will be zero.</li>
<li>For the VMR-9, the number of allocated surfaces is <b>dwMinNumSurfaces</b>.</li>
</ul>
Initially, the decoder should set <b>dwMinNumSurfaces</b> equal to the optimal number of surfaces needed to decode smoothly. If the renderer cannot allocate that many surfaces, the connection will fail with the error code E_OUTOFMEMORY. The decoder should reconnect with the same media type but set <b>dwMinNumSurfaces</b> equal to the minimum number of surfaces required for decoding. For example, the optimal number of surfaces might be 8, while the minimum is 4.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/ee8cbe71-6ac3-4f41-a9af-f372f825485d">IAMVideoAcceleratorNotify::GetUncompSurfacesInfo</a>
 

 

