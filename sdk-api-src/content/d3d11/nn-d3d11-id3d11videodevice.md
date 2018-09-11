---
UID: NN:d3d11.ID3D11VideoDevice
title: ID3D11VideoDevice
author: windows-sdk-content
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videodevice.htm
tech.root: medfound
ms.assetid: 420DE3C4-15A9-4EEB-A1FD-6350DE109CFF
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoDevice, ID3D11VideoDevice interface [Media Foundation], ID3D11VideoDevice interface [Media Foundation],described, d3d11/ID3D11VideoDevice, mf.id3d11videodevice
ms.prod: windows
ms.technology: windows-sdk
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11VideoDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Hh447784(v=VS.85).aspx">CreateAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Creates a channel to communicate with the Direct3D device or the graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447785(v=VS.85).aspx">CreateCryptoSession</a>
</td>
<td align="left" width="63%">
Creates a cryptographic session to encrypt video content that is sent to the graphics driver.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447786(v=VS.85).aspx">CreateVideoDecoder</a>
</td>
<td align="left" width="63%">
Creates a video decoder device for Direct3D 11.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447787(v=VS.85).aspx">CreateVideoDecoderOutputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video decoder, describing the output sample for the decoding operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a video processor device for Direct3D 11.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447789(v=VS.85).aspx">CreateVideoProcessorEnumerator</a>
</td>
<td align="left" width="63%">
Enumerates the video processor capabilities of the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447790(v=VS.85).aspx">CreateVideoProcessorInputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video processor, describing the input sample for the video processing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447791(v=VS.85).aspx">CreateVideoProcessorOutputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video processor, describing the output sample for the video processing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447792(v=VS.85).aspx">GetContentProtectionCaps</a>
</td>
<td align="left" width="63%">
Queries the driver for its content protection capabilities.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447793(v=VS.85).aspx">GetVideoDecoderConfig</a>
</td>
<td align="left" width="63%">
Gets a decoder configuration that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447794(v=VS.85).aspx">GetVideoDecoderConfigCount</a>
</td>
<td align="left" width="63%">
Gets the number of decoder configurations that the driver supports for a specified video description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447795(v=VS.85).aspx">GetVideoDecoderProfile</a>
</td>
<td align="left" width="63%">
Gets a profile that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447796(v=VS.85).aspx">GetVideoDecoderProfileCount</a>
</td>
<td align="left" width="63%">
Gets the number of profiles that are supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447797(v=VS.85).aspx">SetPrivateData</a>
</td>
<td align="left" width="63%">
Sets private data on the video device and associates that data with a GUID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447798(v=VS.85).aspx">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Sets a private <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer on the video device and associates that pointer with a GUID.


</td>
</tr>
</table> 


## -remarks



The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> with an <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a> interface pointer.

If you query an <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a> for <b>ID3D11VideoDevice</b> and the Direct3D 11 device created is using the reference rasterizer or WARP, or is a hardware device and you are using the Microsoft Basic Display Adapter, <b>E_NOINTERFACE</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn894141(v=VS.85).aspx">ID3D11VideoDevice1</a>
 

 

