---
UID: NF:dxva2api.IDirectXVideoDecoder.ReleaseBuffer
title: IDirectXVideoDecoder::ReleaseBuffer
author: windows-sdk-content
description: Releases a buffer that was obtained by calling IDirectXVideoDecoder::GetBuffer.
old-location: mf\idirectxvideodecoder_releasebuffer.htm
tech.root: medfound
ms.assetid: e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IDirectXVideoDecoder interface [Media Foundation],ReleaseBuffer method, IDirectXVideoDecoder.ReleaseBuffer, IDirectXVideoDecoder::ReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [Media Foundation], ReleaseBuffer method [Media Foundation],IDirectXVideoDecoder interface, dxva2api/IDirectXVideoDecoder::ReleaseBuffer, e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90, mf.idirectxvideodecoder_releasebuffer
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
 - IDirectXVideoDecoder.ReleaseBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoDecoder::ReleaseBuffer


## -description


Releases a buffer that was obtained by calling <a href="https://msdn.microsoft.com/db2d4818-8a96-461e-88c4-f25d3200d815">IDirectXVideoDecoder::GetBuffer</a>.
        


## -parameters




### -param BufferType [in]

The type of buffer to release. Specify the same value that was used in the <i>BufferType</i> parameter of the <a href="https://msdn.microsoft.com/db2d4818-8a96-461e-88c4-f25d3200d815">GetBuffer</a> method.


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
 

 

