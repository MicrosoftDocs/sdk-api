---
UID: NS:amva._tag_AMVACompBufferInfo
title: "_tag_AMVACompBufferInfo"
author: windows-driver-content
description: The AMVACompBufferInfo structure describes the allocated surfaces and compressed buffer information.
old-location: dshow\amvacompbufferinfo.htm
old-project: DirectShow
ms.assetid: 74ef5dfb-1062-40c6-a2dd-76f46ca8db92
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: "*LPAMVACompBufferInfo, AMVACompBufferInfo, AMVACompBufferInfo structure [DirectShow], AMVACompBufferInfoStructure, LPAMVACompBufferInfo, LPAMVACompBufferInfo structure pointer [DirectShow], _tag_AMVACompBufferInfo, amva/AMVACompBufferInfo, amva/LPAMVACompBufferInfo, dshow.amvacompbufferinfo"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AMVACompBufferInfo, *LPAMVACompBufferInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	amva.h
api_name:
-	AMVACompBufferInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _tag_AMVACompBufferInfo structure


## -description



          The <b>AMVACompBufferInfo</b> structure describes the allocated surfaces and compressed buffer information.


## -struct-fields




### -field dwNumCompBuffers


            Number of buffers requested for compressed data.
          


### -field dwWidthToCreate


            Width of surface to create.
          


### -field dwHeightToCreate


            Height of surface to create.
          


### -field dwBytesToAllocate


            Total number of bytes used by each surface.
          


### -field ddCompCaps

<b>DDSCAPS2</b> structure defining the capabilities of the DirectDraw surface created to store compressed data.
          


### -field ddPixelFormat

<b>DDPIXELFORMAT</b> structure, describing the pixel format used to create surfaces to store compressed data.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/c32fb94d-396f-460a-9e69-1baaf14eff6e">IAMVideoAccelerator::GetCompBufferInfo</a>
 

 

