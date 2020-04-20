---
UID: NF:dxva2api.IDirectXVideoDecoder.EndFrame
title: IDirectXVideoDecoder::EndFrame (dxva2api.h)
description: Signals the end of the decoding operation.helpviewer_keywords: ["4b8d391e-b679-4adb-8b01-2899996ede46","EndFrame","EndFrame method [Media Foundation]","EndFrame method [Media Foundation]","IDirectXVideoDecoder interface","IDirectXVideoDecoder interface [Media Foundation]","EndFrame method","IDirectXVideoDecoder.EndFrame","IDirectXVideoDecoder::EndFrame","dxva2api/IDirectXVideoDecoder::EndFrame","mf.idirectxvideodecoder_endframe"]
old-location: mf\idirectxvideodecoder_endframe.htm
tech.root: medfound
ms.assetid: 4b8d391e-b679-4adb-8b01-2899996ede46
ms.date: 12/05/2018
ms.keywords: 4b8d391e-b679-4adb-8b01-2899996ede46, EndFrame, EndFrame method [Media Foundation], EndFrame method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],EndFrame method, IDirectXVideoDecoder.EndFrame, IDirectXVideoDecoder::EndFrame, dxva2api/IDirectXVideoDecoder::EndFrame, mf.idirectxvideodecoder_endframe
f1_keywords:
- dxva2api/IDirectXVideoDecoder.EndFrame
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dxva2api.h
api_name:
- IDirectXVideoDecoder.EndFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoDecoder::EndFrame


## -description


Signals the end of the decoding operation.
        


## -parameters




### -param pHandleComplete [out]

Reserved.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a>
 

 

