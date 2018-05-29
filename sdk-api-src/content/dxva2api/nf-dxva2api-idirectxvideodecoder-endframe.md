---
UID: NF:dxva2api.IDirectXVideoDecoder.EndFrame
title: IDirectXVideoDecoder::EndFrame
author: windows-sdk-content
description: Signals the end of the decoding operation.
old-location: mf\idirectxvideodecoder_endframe.htm
old-project: medfound
ms.assetid: 4b8d391e-b679-4adb-8b01-2899996ede46
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 4b8d391e-b679-4adb-8b01-2899996ede46, EndFrame, EndFrame method [Media Foundation], EndFrame method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],EndFrame method, IDirectXVideoDecoder.EndFrame, IDirectXVideoDecoder::EndFrame, dxva2api/IDirectXVideoDecoder::EndFrame, mf.idirectxvideodecoder_endframe
ms.prod: windows
ms.technology: windows-sdk
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
-	IDirectXVideoDecoder.EndFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
 

 

