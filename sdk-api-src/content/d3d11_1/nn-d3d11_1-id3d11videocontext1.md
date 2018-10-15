---
UID: NN:d3d11_1.ID3D11VideoContext1
title: ID3D11VideoContext1
author: windows-sdk-content
description: Provides the video functionality of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videocontext1.htm
tech.root: medfound
ms.assetid: 64D12F68-C2AA-4C1D-9608-5F97CF7AD430
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID3D11VideoContext1, ID3D11VideoContext1 interface [Media Foundation], ID3D11VideoContext1 interface [Media Foundation],described, d3d11_1/ID3D11VideoContext1, mf.id3d11videocontext1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext1 interface


## -description


Provides the video functionality of a Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>. <b>ID3D11VideoContext1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn894127(v=VS.85).aspx">CheckCryptoSessionStatus</a>
</td>
<td align="left" width="63%">
Checks the status of a crypto session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894128(v=VS.85).aspx">DecoderEnableDownsampling</a>
</td>
<td align="left" width="63%">
Indicates that decoder downsampling will be used and that the driver should allocate the appropriate reference frames.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894129(v=VS.85).aspx">DecoderUpdateDownsampling</a>
</td>
<td align="left" width="63%">
Updates the decoder downsampling parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894130(v=VS.85).aspx">GetDataForNewHardwareKey</a>
</td>
<td align="left" width="63%">
Allows the driver to return IHV specific information used when initializing the new hardware key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894131(v=VS.85).aspx">SubmitDecoderBuffers1</a>
</td>
<td align="left" width="63%">
Submits one or more buffers for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894132(v=VS.85).aspx">VideoProcessorGetBehaviorHints</a>
</td>
<td align="left" width="63%">
Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than <a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894133(v=VS.85).aspx">VideoProcessorGetOutputColorSpace1</a>
</td>
<td align="left" width="63%">
Gets the color space information for the video processor output surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894134(v=VS.85).aspx">VideoProcessorGetOutputShaderUsage</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the output surface from a call to <a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorBlt</a> can be read by Direct3D shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894135(v=VS.85).aspx">VideoProcessorGetStreamColorSpace1</a>
</td>
<td align="left" width="63%">
Gets the color space information for the video processor input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894136(v=VS.85).aspx">VideoProcessorGetStreamMirror</a>
</td>
<td align="left" width="63%">
Gets values that indicate whether the video processor input stream is  being flipped vertically or horizontally.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894137(v=VS.85).aspx">VideoProcessorSetOutputColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space information for the video processor output surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894138(v=VS.85).aspx">VideoProcessorSetOutputShaderUsage</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether the output surface from a call to <a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894139(v=VS.85).aspx">VideoProcessorSetStreamColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space information for the video processor input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn894140(v=VS.85).aspx">VideoProcessorSetStreamMirror</a>
</td>
<td align="left" width="63%">
Specifies whether the video processor input stream should be flipped vertically or horizontally.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> with an <a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>  interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

