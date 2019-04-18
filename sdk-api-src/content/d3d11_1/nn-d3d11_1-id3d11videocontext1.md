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
ms.custom: 19H1
---

# ID3D11VideoContext1 interface


## -description


Provides the video functionality of a Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoContext1</b> interface inherits from <a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>. <b>ID3D11VideoContext1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/07126C45-2771-432C-9644-FD4099B8D26D">CheckCryptoSessionStatus</a>
</td>
<td align="left" width="63%">
Checks the status of a crypto session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0BE7E6EC-E090-4A13-9D18-108BDBBC211A">DecoderEnableDownsampling</a>
</td>
<td align="left" width="63%">
Indicates that decoder downsampling will be used and that the driver should allocate the appropriate reference frames.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A55D652B-9295-42E4-9A83-CAC467BEE68E">DecoderUpdateDownsampling</a>
</td>
<td align="left" width="63%">
Updates the decoder downsampling parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4C02F80C-CF7A-4E66-9172-D55A31986ACD">GetDataForNewHardwareKey</a>
</td>
<td align="left" width="63%">
Allows the driver to return IHV specific information used when initializing the new hardware key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9E5FC926-71D7-4102-8952-EC0585B4A4FC">SubmitDecoderBuffers1</a>
</td>
<td align="left" width="63%">
Submits one or more buffers for decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DDA8B3DE-A9D2-48A5-ABEE-E3F7A0EEB965">VideoProcessorGetBehaviorHints</a>
</td>
<td align="left" width="63%">
Returns driver hints that indicate which of the video processor operations are best performed using multi-plane overlay hardware rather than <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B2BC801-CC5C-460C-A10E-CCDEE35A8E27">VideoProcessorGetOutputColorSpace1</a>
</td>
<td align="left" width="63%">
Gets the color space information for the video processor output surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B75BDC83-3065-41F8-B552-B38BCB4BFC66">VideoProcessorGetOutputShaderUsage</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the output surface from a call to <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> can be read by Direct3D shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C9A53D81-C3E4-4B6F-9189-A58E40F8B7E7">VideoProcessorGetStreamColorSpace1</a>
</td>
<td align="left" width="63%">
Gets the color space information for the video processor input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DAB96601-C1B5-4B23-BD88-0C5CB515E842">VideoProcessorGetStreamMirror</a>
</td>
<td align="left" width="63%">
Gets values that indicate whether the video processor input stream is  being flipped vertically or horizontally.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8DDD17AD-997F-406F-B337-E2256F67FC66">VideoProcessorSetOutputColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space information for the video processor output surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84901282-D4FF-4084-B016-50A66910D0A2">VideoProcessorSetOutputShaderUsage</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether the output surface from a call to <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5B1B6FFC-4BC7-4C6D-B3A8-A552D64448E4">VideoProcessorSetStreamColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space information for the video processor input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8CCCC2B-B05A-4AF4-9274-1E205B9807DB">VideoProcessorSetStreamMirror</a>
</td>
<td align="left" width="63%">
Specifies whether the video processor input stream should be flipped vertically or horizontally.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> with an <a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>  interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>



<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

