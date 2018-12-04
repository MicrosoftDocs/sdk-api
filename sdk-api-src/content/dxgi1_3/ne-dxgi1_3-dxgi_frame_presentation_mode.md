---
UID: NE:dxgi1_3.DXGI_FRAME_PRESENTATION_MODE
title: DXGI_FRAME_PRESENTATION_MODE
author: windows-sdk-content
description: Indicates options for presenting frames to the swap chain.
old-location: direct3ddxgi\dxgi_frame_presentation_mode.htm
tech.root: direct3ddxgi
ms.assetid: F9D26722-E8E8-4A2F-A411-D461B96F3F9C
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DXGI_FRAME_PRESENTATION_MODE, DXGI_FRAME_PRESENTATION_MODE enumeration [DXGI], DXGI_FRAME_PRESENTATION_MODE_COMPOSED, DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE, DXGI_FRAME_PRESENTATION_MODE_NONE, DXGI_FRAME_PRESENTATION_MODE_OVERLAY, direct3ddxgi.dxgi_frame_presentation_mode, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_COMPOSED, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_NONE, dxgi1_3/DXGI_FRAME_PRESENTATION_MODE_OVERLAY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_FRAME_PRESENTATION_MODE
product: Windows
targetos: Windows
req.typenames: DXGI_FRAME_PRESENTATION_MODE
req.redist: 
---

# DXGI_FRAME_PRESENTATION_MODE enumeration


## -description


Indicates options for presenting frames to the swap chain.
        


## -enum-fields




### -field DXGI_FRAME_PRESENTATION_MODE_COMPOSED

Specifies that the presentation mode is a composition surface, meaning that the conversion from YUV to RGB is happening once per output refresh (for example, 60 Hz).
            When this value is returned, the media app should discontinue use of the decode swap chain and perform YUV to RGB conversion itself, reducing the frequency of YUV to RGB conversion to once per video frame.
          


### -field DXGI_FRAME_PRESENTATION_MODE_OVERLAY

Specifies that the presentation mode is an overlay surface, meaning that the YUV to RGB conversion is happening efficiently in hardware (once per video frame).
            When this value is returned, the media app can continue to use the decode swap chain.
            See <a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>.
          


### -field DXGI_FRAME_PRESENTATION_MODE_NONE

No presentation is specified.
          


### -field DXGI_FRAME_PRESENTATION_MODE_COMPOSITION_FAILURE

An  issue occurred that caused content protection to be invalidated in a swap-chain with hardware content protection, and is usually because the system ran out of hardware protected memory. The app will need to do one of the following:

<ul>
<li>Drastically reduce the amount of hardware protected memory used. For example, media applications might be able to reduce their buffering.
</li>
<li>Stop using hardware protection if possible.</li>
</ul>
Note that simply re-creating the swap chain or the device will usually have no impact as the DWM will continue to run out of memory and will return the same failure.




## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/BC23B5C1-8257-4556-B930-E09FE60D536C">DXGI_FRAME_STATISTICS_MEDIA</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

