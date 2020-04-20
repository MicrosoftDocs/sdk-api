---
UID: NN:d3d11.ID3D11VideoDevice
title: ID3D11VideoDevice (d3d11.h)
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.helpviewer_keywords: ["ID3D11VideoDevice","ID3D11VideoDevice interface [Media Foundation]","ID3D11VideoDevice interface [Media Foundation]","described","d3d11/ID3D11VideoDevice","mf.id3d11videodevice"]
old-location: mf\id3d11videodevice.htm
tech.root: medfound
ms.assetid: 420DE3C4-15A9-4EEB-A1FD-6350DE109CFF
ms.date: 12/05/2018
ms.keywords: ID3D11VideoDevice, ID3D11VideoDevice interface [Media Foundation], ID3D11VideoDevice interface [Media Foundation],described, d3d11/ID3D11VideoDevice, mf.id3d11videodevice
f1_keywords:
- d3d11/ID3D11VideoDevice
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoDevice interface


## -description


Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11VideoDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange">CheckCryptoKeyExchange</a>
</td>
<td align="left" width="63%">
Gets a cryptographic key-exchange mechanism that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat">CheckVideoDecoderFormat</a>
</td>
<td align="left" width="63%">
Given aprofile, checks whether the driver supports a specified output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel">CreateAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Creates a channel to communicate with the Direct3D device or the graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession">CreateCryptoSession</a>
</td>
<td align="left" width="63%">
Creates a cryptographic session to encrypt video content that is sent to the graphics driver.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">CreateVideoDecoder</a>
</td>
<td align="left" width="63%">
Creates a video decoder device for Direct3D 11.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview">CreateVideoDecoderOutputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video decoder, describing the output sample for the decoding operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a video processor device for Direct3D 11.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">CreateVideoProcessorEnumerator</a>
</td>
<td align="left" width="63%">
Enumerates the video processor capabilities of the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview">CreateVideoProcessorInputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video processor, describing the input sample for the video processing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview">CreateVideoProcessorOutputView</a>
</td>
<td align="left" width="63%">
Creates a resource view for a video processor, describing the output sample for the video processing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">GetContentProtectionCaps</a>
</td>
<td align="left" width="63%">
Queries the driver for its content protection capabilities.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig">GetVideoDecoderConfig</a>
</td>
<td align="left" width="63%">
Gets a decoder configuration that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount">GetVideoDecoderConfigCount</a>
</td>
<td align="left" width="63%">
Gets the number of decoder configurations that the driver supports for a specified video description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">GetVideoDecoderProfile</a>
</td>
<td align="left" width="63%">
Gets a profile that is supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount">GetVideoDecoderProfileCount</a>
</td>
<td align="left" width="63%">
Gets the number of profiles that are supported by the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata">SetPrivateData</a>
</td>
<td align="left" width="63%">
Sets private data on the video device and associates that data with a GUID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Sets a private <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer on the video device and associates that pointer with a GUID.


</td>
</tr>
</table> 


## -remarks



The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> interface pointer.

If you query an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> for <b>ID3D11VideoDevice</b> and the Direct3D 11 device created is using the reference rasterizer or WARP, or is a hardware device and you are using the Microsoft Basic Display Adapter, <b>E_NOINTERFACE</b> is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videodevice1">ID3D11VideoDevice1</a>
 

 

