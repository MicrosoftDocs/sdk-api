---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDXGIDecodeSwapChain::PresentBuffer


## -description


Presents a frame on the output adapter. The frame is a subresource of the <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> object that was used to create the decode swap chain.


## -parameters




### -param BufferToPresent

An index indicating which member of the subresource array to present.


### -param SyncInterval

An integer that specifies how to synchronize presentation of a frame with the vertical blank.


For the bit-block transfer (bitblt) model (<a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_DISCARD</a>
or <a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_SEQUENTIAL</a>), values are:

<ul>
<li>0 - The presentation occurs immediately, there is no synchronization.</li>
<li>1,2,3,4 - Synchronize presentation after the <i>n</i>th vertical blank.</li>
</ul>
For the flip model (<a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>), values are:

<ul>
<li>0 - Cancel the remaining time on the previously presented frame and discard this frame if a newer frame is queued.
</li>
<li>n &gt; 0 - Synchronize presentation for at least <i>n</i> vertical blanks.</li>
</ul>

### -param Flags

An integer value that contains swap-chain presentation options. These options are defined by the <a href="https://msdn.microsoft.com/1ddf8643-ea3e-4c9f-8439-c245942f7333">DXGI_PRESENT</a> constants.

The <b>DXGI_PRESENT_USE_DURATION</b> flag must be set if a custom present duration (custom refresh rate) is being used.


## -returns



This method returns <b>S_OK</b> on success, or it returns one of the following error codes:

<ul>
<li><a href="dxgi_error.htm">DXGI_ERROR_DEVICE_REMOVED</a></li>
<li><a href="dxgi_status.htm">DXGI_STATUS_OCCLUDED</a></li>
<li><a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a></li>
<li><b>E_OUTOFMEMORY</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

