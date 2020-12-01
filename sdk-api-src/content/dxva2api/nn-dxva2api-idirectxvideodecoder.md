---
UID: NN:dxva2api.IDirectXVideoDecoder
title: IDirectXVideoDecoder (dxva2api.h)
description: Represents a DirectX Video Acceleration (DXVA) video decoder device.
helpviewer_keywords: ["116c19a3-39be-4f96-969f-f3d62ed33a70","IDirectXVideoDecoder","IDirectXVideoDecoder interface [Media Foundation]","IDirectXVideoDecoder interface [Media Foundation]","described","dxva2api/IDirectXVideoDecoder","mf.idirectxvideodecoder"]
old-location: mf\idirectxvideodecoder.htm
tech.root: mf
ms.assetid: 116c19a3-39be-4f96-969f-f3d62ed33a70
ms.date: 12/05/2018
ms.keywords: 116c19a3-39be-4f96-969f-f3d62ed33a70, IDirectXVideoDecoder, IDirectXVideoDecoder interface [Media Foundation], IDirectXVideoDecoder interface [Media Foundation],described, dxva2api/IDirectXVideoDecoder, mf.idirectxvideodecoder
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectXVideoDecoder
 - dxva2api/IDirectXVideoDecoder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoDecoder
---

# IDirectXVideoDecoder interface


## -description

Represents a DirectX Video Acceleration (DXVA) video decoder device.

 To get a pointer to this interface, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder">IDirectXVideoDecoderService::CreateVideoDecoder</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectXVideoDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe">BeginFrame</a>
</td>
<td align="left" width="63%">
Starts the decoding operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-endframe">EndFrame</a>
</td>
<td align="left" width="63%">
Signals the end of the decoding operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute">Execute</a>
</td>
<td align="left" width="63%">
Executes a decoding operation on the current frame.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a DXVA decoder buffer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getcreationparameters">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Gets the parameters that were used to create this device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getvideodecoderservice">GetVideoDecoderService</a>
</td>
<td align="left" width="63%">
Gets the DXVA decoder service that created this decoder device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was obtained by calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer">GetBuffer</a>.
        

</td>
</tr>
</table>

## -remarks

The <b>IDirectXVideoDecoder</b> methods make calls to the Direct3D device. Therefore, the <b>D3DCREATE</b> flags that you specify  when creating the device can affect the behavior of this interface. For example, if you specify the <b>D3DCREATE_MULTITHREADED</b> flag, the Direct3D global critical section will be held during decode operations.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>