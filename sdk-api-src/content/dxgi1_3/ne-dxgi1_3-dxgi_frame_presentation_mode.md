---
UID: NE:dxgi1_3.DXGI_FRAME_PRESENTATION_MODE
title: DXGI_FRAME_PRESENTATION_MODE (dxgi1_3.h)
description: Indicates options for presenting frames to the swap chain.
helpviewer_keywords: ["DXGI_FRAME_PRESENTATION_MODE","DXGI_FRAME_PRESENTATION_MODE enumeration [DXGI]","DXGI_FRAME_PRESENTATION_MODE_COMPOSED","DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE","DXGI_FRAME_PRESENTATION_MODE_NONE","DXGI_FRAME_PRESENTATION_MODE_OVERLAY","direct3ddxgi.dxgi_frame_presentation_mode","dxgi1_3/DXGI_FRAME_PRESENTATION_MODE","dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_COMPOSED","dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE","dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_NONE","dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_OVERLAY"]
old-location: direct3ddxgi\dxgi_frame_presentation_mode.htm
tech.root: direct3ddxgi
ms.assetid: F9D26722-E8E8-4A2F-A411-D461B96F3F9C
ms.date: 12/05/2018
ms.keywords: DXGI_FRAME_PRESENTATION_MODE, DXGI_FRAME_PRESENTATION_MODE enumeration [DXGI], DXGI_FRAME_PRESENTATION_MODE_COMPOSED, DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE, DXGI_FRAME_PRESENTATION_MODE_NONE, DXGI_FRAME_PRESENTATION_MODE_OVERLAY, direct3ddxgi.dxgi_frame_presentation_mode, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_COMPOSED, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_NONE, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_OVERLAY
req.header: dxgi1_3.h
req.include-header: DXGIPartner.h
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
req.typenames: DXGI_FRAME_PRESENTATION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_FRAME_PRESENTATION_MODE
 - dxgi1_3/DXGI_FRAME_PRESENTATION_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_FRAME_PRESENTATION_MODE
---

# DXGI_FRAME_PRESENTATION_MODE enumeration


## -description

Indicates options for presenting frames to the swap chain.

## -enum-fields

### -field DXGI_FRAME_PRESENTATION_MODE_COMPOSED:0

Specifies that the presentation mode is a composition surface, meaning that the conversion from YUV to RGB is happening once per output refresh (for example, 60 Hz).
            When this value is returned, the media app should discontinue use of the decode swap chain and perform YUV to RGB conversion itself, reducing the frequency of YUV to RGB conversion to once per video frame.

### -field DXGI_FRAME_PRESENTATION_MODE_OVERLAY:1

Specifies that the presentation mode is an overlay surface, meaning that the YUV to RGB conversion is happening efficiently in hardware (once per video frame).
            When this value is returned, the media app can continue to use the decode swap chain.
            See <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>.

### -field DXGI_FRAME_PRESENTATION_MODE_NONE:2

No presentation is specified.

### -field DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE:3

An  issue occurred that caused content protection to be invalidated in a swap-chain with hardware content protection, and is usually because the system ran out of hardware protected memory. The app will need to do one of the following:

<ul>
<li>Drastically reduce the amount of hardware protected memory used. For example, media applications might be able to reduce their buffering.
</li>
<li>Stop using hardware protection if possible.</li>
</ul>
Note that simply re-creating the swap chain or the device will usually have no impact as the DWM will continue to run out of memory and will return the same failure.

## -remarks

This enum is used by the <a href="/windows/desktop/api/dxgi1_3/ns-dxgi1_3-dxgi_frame_statistics_media">DXGI_FRAME_STATISTICS_MEDIA</a> structure.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
