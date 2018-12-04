---
UID: NF:dxva2api.IDirectXVideoDecoder.GetVideoDecoderService
title: IDirectXVideoDecoder::GetVideoDecoderService
author: windows-sdk-content
description: Retrieves the DirectX Video Acceleration (DXVA) decoder service that created this decoder device.
old-location: mf\idirectxvideodecoder_getvideodecoderservice.htm
tech.root: medfound
ms.assetid: 092c49cd-6bfc-4ed0-9378-5751ad19296c
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 092c49cd-6bfc-4ed0-9378-5751ad19296c, GetVideoDecoderService, GetVideoDecoderService method [Media Foundation], GetVideoDecoderService method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],GetVideoDecoderService method, IDirectXVideoDecoder.GetVideoDecoderService, IDirectXVideoDecoder::GetVideoDecoderService, dxva2api/IDirectXVideoDecoder::GetVideoDecoderService, mf.idirectxvideodecoder_getvideodecoderservice
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
 - IDirectXVideoDecoder.GetVideoDecoderService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoDecoder::GetVideoDecoderService


## -description


Retrieves the DirectX Video Acceleration (DXVA) decoder service that created this decoder device.
        


## -parameters




### -param ppService [out]

Receives a pointer to <a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
 

 

