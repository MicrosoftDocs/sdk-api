---
UID: NF:dxva2api.IDirectXVideoDecoder.BeginFrame
title: IDirectXVideoDecoder::BeginFrame
author: windows-driver-content
description: Starts the decoding operation.
old-location: mf\idirectxvideodecoder_beginframe.htm
old-project: medfound
ms.assetid: 17759e7b-e6d4-4270-abd3-0f73c1df7ccb
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 17759e7b-e6d4-4270-abd3-0f73c1df7ccb, BeginFrame, BeginFrame method [Media Foundation], BeginFrame method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],BeginFrame method, IDirectXVideoDecoder.BeginFrame, IDirectXVideoDecoder::BeginFrame, dxva2api/IDirectXVideoDecoder::BeginFrame, mf.idirectxvideodecoder_beginframe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DXVA2_SurfaceType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva2api.h
api_name:
-	IDirectXVideoDecoder.BeginFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoDecoder::BeginFrame


## -description



          Starts the decoding operation.
        


## -parameters




### -param pRenderTarget [in]

Pointer to the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface of the render target where the decoded frame will be written.


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



After this method is called, call <a href="https://msdn.microsoft.com/3c957b2f-4bba-4c39-84de-719c08e1bf78">IDirectXVideoDecoder::Execute</a> to perform decoding operations. When all decoding operations have been executed, call <a href="https://msdn.microsoft.com/4b8d391e-b679-4adb-8b01-2899996ede46">IDirectXVideoDecoder::EndFrame</a>.

Each call to <b>BeginFrame</b> must have a matching call to <a href="https://msdn.microsoft.com/4b8d391e-b679-4adb-8b01-2899996ede46">EndFrame</a>, and <b>BeginFrame</b> calls cannot be nested.

DXVA 1.0 migration note: Unlike the <b>IAMVideoAccelerator::BeginFrame</b> method, which specifies the buffer as an index, this method takes a pointer directly to the uncompressed buffer.

The surface pointed to by <i>pRenderTarget</i> must be created by calling <a href="https://msdn.microsoft.com/34ed2029-7c79-45ce-962d-df4970babb23">IDirectXVideoAccelerationService::CreateSurface</a> with the value DXVA2_VideoDecoderRenderTarget for <i>DxvaType</i>.




## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
 

 

