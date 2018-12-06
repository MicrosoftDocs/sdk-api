---
UID: NN:videoacc.IAMVideoAccelerator
title: IAMVideoAccelerator
author: windows-sdk-content
description: The IAMVideoAccelerator interface enables a video decoder filter to access DirectX Video Acceleration (DXVA) 1.0 functionality.
old-location: dshow\iamvideoaccelerator.htm
tech.root: DirectShow
ms.assetid: 78e0a165-5a19-4dca-8d6c-445345772824
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMVideoAccelerator, IAMVideoAccelerator interface [DirectShow], IAMVideoAccelerator interface [DirectShow],described, IAMVideoAcceleratorInterface, dshow.iamvideoaccelerator, videoacc/IAMVideoAccelerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAccelerator interface


## -description



The <b>IAMVideoAccelerator</b> interface enables a video decoder filter to access DirectX Video Acceleration (DXVA) 1.0 functionality. Applications should not call methods on this interface.

The Video Mixing Renderer filter's input pins support this interface, and so does pin 0 on the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>. If a video decoder filter calls methods on this interface, the decoder should support the <a href="https://msdn.microsoft.com/7fd0290c-8fd6-4af6-b510-7a87bc7937de">IAMVideoAcceleratorNotify</a> interface on its output pin. For more information on how to use this interface, see <a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoAccelerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVideoAccelerator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/00077ffe-4acb-4648-9e95-652184e4449b">BeginFrame</a>
</td>
<td align="left" width="63%">
Begins the processing to create a decoded picture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7913401f-881a-4364-8504-b02e85a5e343">DisplayFrame</a>
</td>
<td align="left" width="63%">
Causes the video renderer to display a decoded frame

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38944989-2ce2-4275-bae9-faca0d51cca8">EndFrame</a>
</td>
<td align="left" width="63%">
Ends frame processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12794739-9120-4dc1-b95d-6d390d25726b">Execute</a>
</td>
<td align="left" width="63%">
Performs a decompression operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3385cad2-8885-4b17-83fa-f40f25b0c433">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a compressed or uncompressed surface that was allocated for DXVA decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c32fb94d-396f-460a-9e69-1baaf14eff6e">GetCompBufferInfo</a>
</td>
<td align="left" width="63%">
Gets information about the compressed buffers used for DXVA decoding. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b60c6bf7-6cb6-4a82-bec4-7f1662d4ee95">GetInternalCompBufferInfo</a>
</td>
<td align="left" width="63%">
After the pins are connected, gets information about the compressed buffers used for DXVA decoding. 

<div class="alert"><b>Note</b>  Unlike <a href="https://msdn.microsoft.com/c32fb94d-396f-460a-9e69-1baaf14eff6e">GetCompBufferInfo</a>, this method cannot be called during the pin connection process.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64b6371c-4baf-4ec1-bd0d-6413f053e2fa">GetInternalMemInfo</a>
</td>
<td align="left" width="63%">
Queries for the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33f9a4ee-4de9-4853-9581-808d7a07bfc4">GetUncompFormatsSupported</a>
</td>
<td align="left" width="63%">
Retrieves a list of pixel formats that can be used to render a specified video accelerator format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/808ba120-f0e1-4348-94e7-69a27c77cf42">GetVideoAcceleratorGUIDs</a>
</td>
<td align="left" width="63%">
Gets a list of DirectX Video Acceleration (DXVA) profiles supported by the display driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29d77bd5-2823-4e67-a69f-2898ad4c467c">QueryRenderStatus</a>
</td>
<td align="left" width="63%">
Queries the read/write status of a DXVA decoding surface.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2170cf7e-85c8-4658-84fd-96ebc0d2704f">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was locked by a previous call to <a href="https://msdn.microsoft.com/3385cad2-8885-4b17-83fa-f40f25b0c433">GetBuffer</a>.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>
 

 

