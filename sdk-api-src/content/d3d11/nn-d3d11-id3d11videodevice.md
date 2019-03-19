---
UID: NN:d3d11.ID3D11VideoDevice
title: ID3D11VideoDevice (d3d11.h)
author: windows-sdk-content
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videodevice.htm
tech.root: medfound
ms.assetid: 420DE3C4-15A9-4EEB-A1FD-6350DE109CFF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoDevice, ID3D11VideoDevice interface [Media Foundation], ID3D11VideoDevice interface [Media Foundation],described, d3d11/ID3D11VideoDevice, mf.id3d11videodevice
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - ID3D11VideoDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDevice interface


## -description


Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11VideoDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE2DA6F9-6153-43AF-8E61-26FB9DD5A1D1">CheckCryptoKeyExchange</a>
</td>
<td align="left" width="63%">
Gets a cryptographic key-exchange mechanism that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E834DF38-2847-4864-9CFE-A25CAE51C78F">CheckVideoDecoderFormat</a>
</td>
<td align="left" width="63%">
Given aprofile, checks whether the driver supports a specified output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4325E83F-23BF-4104-B30E-27DBE7D23D88">CreateAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Creates a channel to communicate with the Direct3D device or the graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/384EE3E1-2B62-477B-8A3F-FDCD06959B74">CreateCryptoSession</a>
</td>
<td align="left" width="63%">
Creates a cryptographic session to encrypt video content that is sent to the graphics driver.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">CreateVideoDecoder</a>
</td>
<td align="left" width="63%">
Creates a video decoder device for Direct3D 11.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8A3D72CF-B641-4219-8C88-FCE5231CF2F6">CreateVideoDecoderOutputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video decoder, describing the output sample for the decoding operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a video processor device for Direct3D 11.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/992C699D-A499-494E-AEDF-A6688CB14D70">CreateVideoProcessorEnumerator</a>
</td>
<td align="left" width="63%">
Enumerates the video processor capabilities of the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3245D2AF-74A1-4068-A0BC-577FD42B353E">CreateVideoProcessorInputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video processor, describing the input sample for the video processing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC7AFE44-877C-4FB0-9E61-FCD504A334D3">CreateVideoProcessorOutputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video processor, describing the output sample for the video processing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3BF2D2B9-6A12-4E71-9F52-829BABA32EF6">GetContentProtectionCaps</a>
</td>
<td align="left" width="63%">
Queries the driver for its content protection capabilities.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC3B23BE-0A28-41E6-A515-7801C9E0A4D9">GetVideoDecoderConfig</a>
</td>
<td align="left" width="63%">
Gets a decoder configuration that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C6650546-2F6D-4B91-888D-3A5A1AE86DCB">GetVideoDecoderConfigCount</a>
</td>
<td align="left" width="63%">
Gets the number of decoder configurations that the driver supports for a specified video description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8D958469-7FC3-4B4F-82BF-271662CF0088">GetVideoDecoderProfile</a>
</td>
<td align="left" width="63%">
Gets a profile that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6DCAD69B-3C00-4B3A-97AA-69DF26EF5CD4">GetVideoDecoderProfileCount</a>
</td>
<td align="left" width="63%">
Gets the number of profiles that are supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B7B9E225-A27E-4278-B191-08C0C93C86AC">SetPrivateData</a>
</td>
<td align="left" width="63%">
Sets private data on the video device and associates that data with a GUID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E20FC248-92B2-4284-9EDC-9D5E6AB9506B">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Sets a private <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer on the video device and associates that pointer with a GUID.


</td>
</tr>
</table> 


## -remarks



The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> with an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> interface pointer.

If you query an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> for <b>ID3D11VideoDevice</b> and the Direct3D 11 device created is using the reference rasterizer or WARP, or is a hardware device and you are using the Microsoft Basic Display Adapter, <b>E_NOINTERFACE</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/10E68945-6103-491D-8846-3B7C880FEAFD">ID3D11VideoDevice1</a>
 

 

