---
UID: NN:d3d11_1.ID3D11VideoContext1
title: ID3D11VideoContext1 (d3d11_1.h)
author: windows-sdk-content
description: Provides the video functionality of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videocontext1.htm
tech.root: medfound
ms.assetid: 64D12F68-C2AA-4C1D-9608-5F97CF7AD430
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1, ID3D11VideoContext1 interface [Media Foundation], ID3D11VideoContext1 interface [Media Foundation],described, d3d11_1/ID3D11VideoContext1, mf.id3d11videocontext1
ms.topic: interface
f1_keywords: 
 - "d3d11_1/ID3D11VideoContext1"
dev_langs:
 - c++
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext1 interface


## -description


Provides the video functionality of a Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>. <b>ID3D11VideoContext1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoContext1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus">CheckCryptoSessionStatus</a>
</td>
<td align="left" width="63%">
Checks the status of a crypto session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling">DecoderEnableDownsampling</a>
</td>
<td align="left" width="63%">
Indicates that decoder downsampling will be used and that the driver should allocate the appropriate reference frames.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderupdatedownsampling">DecoderUpdateDownsampling</a>
</td>
<td align="left" width="63%">
Updates the decoder downsampling parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey">GetDataForNewHardwareKey</a>
</td>
<td align="left" width="63%">
Allows the driver to return IHV specific information used when initializing the new hardware key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1">SubmitDecoderBuffers1</a>
</td>
<td align="left" width="63%">
Submits one or more buffers for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints">VideoProcessorGetBehaviorHints</a>
</td>
<td align="left" width="63%">
Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1">VideoProcessorGetOutputColorSpace1</a>
</td>
<td align="left" width="63%">
Gets the color space information for the video processor output surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage">VideoProcessorGetOutputShaderUsage</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the output surface from a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> can be read by Direct3D shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1">VideoProcessorGetStreamColorSpace1</a>
</td>
<td align="left" width="63%">
Gets the color space information for the video processor input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror">VideoProcessorGetStreamMirror</a>
</td>
<td align="left" width="63%">
Gets values that indicate whether the video processor input stream is  being flipped vertically or horizontally.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1">VideoProcessorSetOutputColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space information for the video processor output surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage">VideoProcessorSetOutputShaderUsage</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether the output surface from a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1">VideoProcessorSetStreamColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space information for the video processor input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror">VideoProcessorSetStreamMirror</a>
</td>
<td align="left" width="63%">
Specifies whether the video processor input stream should be flipped vertically or horizontally.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> with an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>  interface pointer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

