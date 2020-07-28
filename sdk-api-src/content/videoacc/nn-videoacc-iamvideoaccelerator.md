---
UID: NN:videoacc.IAMVideoAccelerator
title: IAMVideoAccelerator (videoacc.h)
description: The IAMVideoAccelerator interface enables a video decoder filter to access DirectX Video Acceleration (DXVA) 1.0 functionality.
helpviewer_keywords: ["IAMVideoAccelerator","IAMVideoAccelerator interface [DirectShow]","IAMVideoAccelerator interface [DirectShow]","described","IAMVideoAcceleratorInterface","dshow.iamvideoaccelerator","videoacc/IAMVideoAccelerator"]
old-location: dshow\iamvideoaccelerator.htm
tech.root: dshow
ms.assetid: 78e0a165-5a19-4dca-8d6c-445345772824
ms.date: 12/05/2018
ms.keywords: IAMVideoAccelerator, IAMVideoAccelerator interface [DirectShow], IAMVideoAccelerator interface [DirectShow],described, IAMVideoAcceleratorInterface, dshow.iamvideoaccelerator, videoacc/IAMVideoAccelerator
f1_keywords:
- videoacc/IAMVideoAccelerator
dev_langs:
- c++
req.header: videoacc.h
req.include-header: 
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMVideoAccelerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoAccelerator interface


## -description



The <b>IAMVideoAccelerator</b> interface enables a video decoder filter to access DirectX Video Acceleration (DXVA) 1.0 functionality. Applications should not call methods on this interface.

The Video Mixing Renderer filter's input pins support this interface, and so does pin 0 on the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>. If a video decoder filter calls methods on this interface, the decoder should support the <a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify">IAMVideoAcceleratorNotify</a> interface on its output pin. For more information on how to use this interface, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoAccelerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoAccelerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoAccelerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">BeginFrame</a>
</td>
<td align="left" width="63%">
Begins the processing to create a decoded picture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe">DisplayFrame</a>
</td>
<td align="left" width="63%">
Causes the video renderer to display a decoded frame

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe">EndFrame</a>
</td>
<td align="left" width="63%">
Ends frame processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute">Execute</a>
</td>
<td align="left" width="63%">
Performs a decompression operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a compressed or uncompressed surface that was allocated for DXVA decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo">GetCompBufferInfo</a>
</td>
<td align="left" width="63%">
Gets information about the compressed buffers used for DXVA decoding. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getinternalcompbufferinfo">GetInternalCompBufferInfo</a>
</td>
<td align="left" width="63%">
After the pins are connected, gets information about the compressed buffers used for DXVA decoding. 

<div class="alert"><b>Note</b>  Unlike <a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo">GetCompBufferInfo</a>, this method cannot be called during the pin connection process.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getinternalmeminfo">GetInternalMemInfo</a>
</td>
<td align="left" width="63%">
Queries for the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported">GetUncompFormatsSupported</a>
</td>
<td align="left" width="63%">
Retrieves a list of pixel formats that can be used to render a specified video accelerator format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids">GetVideoAcceleratorGUIDs</a>
</td>
<td align="left" width="63%">
Gets a list of DirectX Video Acceleration (DXVA) profiles supported by the display driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus">QueryRenderStatus</a>
</td>
<td align="left" width="63%">
Queries the read/write status of a DXVA decoding surface.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was locked by a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer">GetBuffer</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/gg463516">DXVA 1.0 specification</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>
 

 

