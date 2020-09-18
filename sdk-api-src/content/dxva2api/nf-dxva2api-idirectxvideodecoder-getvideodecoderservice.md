---
UID: NF:dxva2api.IDirectXVideoDecoder.GetVideoDecoderService
title: IDirectXVideoDecoder::GetVideoDecoderService (dxva2api.h)
description: Retrieves the DirectX Video Acceleration (DXVA) decoder service that created this decoder device.
helpviewer_keywords: ["092c49cd-6bfc-4ed0-9378-5751ad19296c","GetVideoDecoderService","GetVideoDecoderService method [Media Foundation]","GetVideoDecoderService method [Media Foundation]","IDirectXVideoDecoder interface","IDirectXVideoDecoder interface [Media Foundation]","GetVideoDecoderService method","IDirectXVideoDecoder.GetVideoDecoderService","IDirectXVideoDecoder::GetVideoDecoderService","dxva2api/IDirectXVideoDecoder::GetVideoDecoderService","mf.idirectxvideodecoder_getvideodecoderservice"]
old-location: mf\idirectxvideodecoder_getvideodecoderservice.htm
tech.root: mf
ms.assetid: 092c49cd-6bfc-4ed0-9378-5751ad19296c
ms.date: 12/05/2018
ms.keywords: 092c49cd-6bfc-4ed0-9378-5751ad19296c, GetVideoDecoderService, GetVideoDecoderService method [Media Foundation], GetVideoDecoderService method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],GetVideoDecoderService method, IDirectXVideoDecoder.GetVideoDecoderService, IDirectXVideoDecoder::GetVideoDecoderService, dxva2api/IDirectXVideoDecoder::GetVideoDecoderService, mf.idirectxvideodecoder_getvideodecoderservice
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
 - IDirectXVideoDecoder::GetVideoDecoderService
 - dxva2api/IDirectXVideoDecoder::GetVideoDecoderService
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
 - IDirectXVideoDecoder.GetVideoDecoderService
---

# IDirectXVideoDecoder::GetVideoDecoderService


## -description

Retrieves the DirectX Video Acceleration (DXVA) decoder service that created this decoder device.

## -parameters

### -param ppService [out]

Receives a pointer to <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a> interface. The caller must release the interface.

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