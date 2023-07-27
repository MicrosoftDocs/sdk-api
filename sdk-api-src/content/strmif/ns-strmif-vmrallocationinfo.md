---
UID: NS:strmif.tagVMRALLOCATIONINFO
title: VMRALLOCATIONINFO (strmif.h)
description: The VMRALLOCATIONINFO structure is used in the VMR-7 filter's IVMRSurfaceAllocator::AllocateSurface method.
helpviewer_keywords: ["VMRALLOCATIONINFO","VMRALLOCATIONINFO structure [DirectShow]","VMRALLOCATIONINFOStructure","dshow.vmrallocationinfo","strmif/VMRALLOCATIONINFO"]
old-location: dshow\vmrallocationinfo.htm
tech.root: dshow
ms.assetid: 3908f9d1-5120-413b-a142-08cd9005c401
ms.date: 4/26/2023
ms.keywords: VMRALLOCATIONINFO, VMRALLOCATIONINFO structure [DirectShow], VMRALLOCATIONINFOStructure, dshow.vmrallocationinfo, strmif/VMRALLOCATIONINFO
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VMRALLOCATIONINFO
req.redist: 
req.product: Windows XP
ms.custom: 19H1
f1_keywords:
 - tagVMRALLOCATIONINFO
 - strmif/tagVMRALLOCATIONINFO
 - VMRALLOCATIONINFO
 - strmif/VMRALLOCATIONINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRALLOCATIONINFO
---

# VMRALLOCATIONINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMRALLOCATIONINFO</code> structure is used in the VMR-7 filter's <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-allocatesurface">IVMRSurfaceAllocator::AllocateSurface</a> method.

## -struct-fields

### -field dwFlags

A bitwise <b>OR</b> of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-vmrsurfaceallocationflags">VMRSurfaceAllocationFlags</a> enumeration.

### -field lpHdr

Pointer to the <b>BITMAPINFOHEADER</b> structure associated with the surface.

### -field lpPixFmt

Pointer to the <b>DDPIXELFORMAT</b> structure associated with the surface.

### -field szAspectRatio

A <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that specifies the aspect ratio of the new surface.

### -field dwMinBuffers

The minimum number of buffers to create for this surface.

### -field dwMaxBuffers

The maximum number of buffers to create for this surface.

### -field dwInterlaceFlags

A bitwise <b>OR</b> of  flags that indicate the interlacing. For a list of flags, see the <b>dwInterlaceFlags</b> member of the <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> structure.

### -field szNativeSize

The size of the native video rectangle.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>