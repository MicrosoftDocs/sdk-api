---
UID: NS:amva._tag_AMVACompBufferInfo
title: AMVACompBufferInfo (amva.h)
description: The AMVACompBufferInfo structure describes the allocated surfaces and compressed buffer information.
helpviewer_keywords: ["*LPAMVACompBufferInfo","AMVACompBufferInfo","AMVACompBufferInfo structure [DirectShow]","AMVACompBufferInfoStructure","LPAMVACompBufferInfo","LPAMVACompBufferInfo structure pointer [DirectShow]","amva/AMVACompBufferInfo","amva/LPAMVACompBufferInfo","dshow.amvacompbufferinfo"]
old-location: dshow\amvacompbufferinfo.htm
tech.root: dshow
ms.assetid: 74ef5dfb-1062-40c6-a2dd-76f46ca8db92
ms.date: 12/05/2018
ms.keywords: '*LPAMVACompBufferInfo, AMVACompBufferInfo, AMVACompBufferInfo structure [DirectShow], AMVACompBufferInfoStructure, LPAMVACompBufferInfo, LPAMVACompBufferInfo structure pointer [DirectShow], amva/AMVACompBufferInfo, amva/LPAMVACompBufferInfo, dshow.amvacompbufferinfo'
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
targetos: Windows
req.typenames: AMVACompBufferInfo, *LPAMVACompBufferInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVACompBufferInfo
 - amva/_tag_AMVACompBufferInfo
 - LPAMVACompBufferInfo
 - amva/LPAMVACompBufferInfo
 - AMVACompBufferInfo
 - amva/AMVACompBufferInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amva.h
api_name:
 - AMVACompBufferInfo
---

# AMVACompBufferInfo structure


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

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo">IAMVideoAccelerator::GetCompBufferInfo</a>