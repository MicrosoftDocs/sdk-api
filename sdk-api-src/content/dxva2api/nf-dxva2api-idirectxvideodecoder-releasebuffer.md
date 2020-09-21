---
UID: NF:dxva2api.IDirectXVideoDecoder.ReleaseBuffer
title: IDirectXVideoDecoder::ReleaseBuffer (dxva2api.h)
description: Releases a buffer that was obtained by calling IDirectXVideoDecoder::GetBuffer.
helpviewer_keywords: ["IDirectXVideoDecoder interface [Media Foundation]","ReleaseBuffer method","IDirectXVideoDecoder.ReleaseBuffer","IDirectXVideoDecoder::ReleaseBuffer","ReleaseBuffer","ReleaseBuffer method [Media Foundation]","ReleaseBuffer method [Media Foundation]","IDirectXVideoDecoder interface","dxva2api/IDirectXVideoDecoder::ReleaseBuffer","e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90","mf.idirectxvideodecoder_releasebuffer"]
old-location: mf\idirectxvideodecoder_releasebuffer.htm
tech.root: mf
ms.assetid: e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90
ms.date: 12/05/2018
ms.keywords: IDirectXVideoDecoder interface [Media Foundation],ReleaseBuffer method, IDirectXVideoDecoder.ReleaseBuffer, IDirectXVideoDecoder::ReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [Media Foundation], ReleaseBuffer method [Media Foundation],IDirectXVideoDecoder interface, dxva2api/IDirectXVideoDecoder::ReleaseBuffer, e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90, mf.idirectxvideodecoder_releasebuffer
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
 - IDirectXVideoDecoder::ReleaseBuffer
 - dxva2api/IDirectXVideoDecoder::ReleaseBuffer
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
 - IDirectXVideoDecoder.ReleaseBuffer
---

# IDirectXVideoDecoder::ReleaseBuffer


## -description

Releases a buffer that was obtained by calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer">IDirectXVideoDecoder::GetBuffer</a>.

## -parameters

### -param BufferType [in]

The type of buffer to release. Specify the same value that was used in the <i>BufferType</i> parameter of the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer">GetBuffer</a> method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a>