---
UID: NF:dxva2api.IDirectXVideoDecoder.Execute
title: IDirectXVideoDecoder::Execute (dxva2api.h)
description: Executes a decoding operation on the current frame.
helpviewer_keywords: ["3c957b2f-4bba-4c39-84de-719c08e1bf78","Execute","Execute method [Media Foundation]","Execute method [Media Foundation]","IDirectXVideoDecoder interface","IDirectXVideoDecoder interface [Media Foundation]","Execute method","IDirectXVideoDecoder.Execute","IDirectXVideoDecoder::Execute","dxva2api/IDirectXVideoDecoder::Execute","mf.idirectxvideodecoder_execute"]
old-location: mf\idirectxvideodecoder_execute.htm
tech.root: mf
ms.assetid: 3c957b2f-4bba-4c39-84de-719c08e1bf78
ms.date: 12/05/2018
ms.keywords: 3c957b2f-4bba-4c39-84de-719c08e1bf78, Execute, Execute method [Media Foundation], Execute method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],Execute method, IDirectXVideoDecoder.Execute, IDirectXVideoDecoder::Execute, dxva2api/IDirectXVideoDecoder::Execute, mf.idirectxvideodecoder_execute
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
 - IDirectXVideoDecoder::Execute
 - dxva2api/IDirectXVideoDecoder::Execute
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
 - IDirectXVideoDecoder.Execute
---

# IDirectXVideoDecoder::Execute


## -description

Executes a decoding operation on the current frame.

## -parameters

### -param pExecuteParams [in]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams">DXVA2_DecodeExecuteParams</a> structure that contains the information needed for the decoding operation.

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

## -remarks

You must call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe">IDirectXVideoDecoder::BeginFrame</a> before calling this method.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a>