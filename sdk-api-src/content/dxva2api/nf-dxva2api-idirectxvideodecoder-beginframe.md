---
UID: NF:dxva2api.IDirectXVideoDecoder.BeginFrame
title: IDirectXVideoDecoder::BeginFrame (dxva2api.h)
description: Starts the decoding operation.
helpviewer_keywords: ["17759e7b-e6d4-4270-abd3-0f73c1df7ccb","BeginFrame","BeginFrame method [Media Foundation]","BeginFrame method [Media Foundation]","IDirectXVideoDecoder interface","IDirectXVideoDecoder interface [Media Foundation]","BeginFrame method","IDirectXVideoDecoder.BeginFrame","IDirectXVideoDecoder::BeginFrame","dxva2api/IDirectXVideoDecoder::BeginFrame","mf.idirectxvideodecoder_beginframe"]
old-location: mf\idirectxvideodecoder_beginframe.htm
tech.root: mf
ms.assetid: 17759e7b-e6d4-4270-abd3-0f73c1df7ccb
ms.date: 12/05/2018
ms.keywords: 17759e7b-e6d4-4270-abd3-0f73c1df7ccb, BeginFrame, BeginFrame method [Media Foundation], BeginFrame method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],BeginFrame method, IDirectXVideoDecoder.BeginFrame, IDirectXVideoDecoder::BeginFrame, dxva2api/IDirectXVideoDecoder::BeginFrame, mf.idirectxvideodecoder_beginframe
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
 - IDirectXVideoDecoder::BeginFrame
 - dxva2api/IDirectXVideoDecoder::BeginFrame
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
 - IDirectXVideoDecoder.BeginFrame
---

# IDirectXVideoDecoder::BeginFrame


## -description

Starts the decoding operation.

## -parameters

### -param pRenderTarget [in]

Pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface of the render target where the decoded frame will be written.

### -param pvPVPData [in]

Reserved; set to <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid surface type. See Remarks.

</td>
</tr>
</table>

## -remarks

After this method is called, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute">IDirectXVideoDecoder::Execute</a> to perform decoding operations. When all decoding operations have been executed, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-endframe">IDirectXVideoDecoder::EndFrame</a>.

Each call to <b>BeginFrame</b> must have a matching call to <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-endframe">EndFrame</a>, and <b>BeginFrame</b> calls cannot be nested.

DXVA 1.0 migration note: Unlike the <b>IAMVideoAccelerator::BeginFrame</b> method, which specifies the buffer as an index, this method takes a pointer directly to the uncompressed buffer.

The surface pointed to by <i>pRenderTarget</i> must be created by calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface">IDirectXVideoAccelerationService::CreateSurface</a> with the value DXVA2_VideoDecoderRenderTarget for <i>DxvaType</i>.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a>