---
UID: NF:dxva2api.IDirectXVideoDecoder.Execute
title: IDirectXVideoDecoder::Execute
author: windows-sdk-content
description: Executes a decoding operation on the current frame.
old-location: mf\idirectxvideodecoder_execute.htm
tech.root: medfound
ms.assetid: 3c957b2f-4bba-4c39-84de-719c08e1bf78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 3c957b2f-4bba-4c39-84de-719c08e1bf78, Execute, Execute method [Media Foundation], Execute method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],Execute method, IDirectXVideoDecoder.Execute, IDirectXVideoDecoder::Execute, dxva2api/IDirectXVideoDecoder::Execute, mf.idirectxvideodecoder_execute
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
 - IDirectXVideoDecoder.Execute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoDecoder::Execute


## -description


Executes a decoding operation on the current frame.
        


## -parameters




### -param pExecuteParams [in]

Pointer to a <a href="https://msdn.microsoft.com/e0e95e9b-6d53-4b90-a933-243023dc31ef">DXVA2_DecodeExecuteParams</a> structure that contains the information needed for the decoding operation.


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



You must call <a href="https://msdn.microsoft.com/17759e7b-e6d4-4270-abd3-0f73c1df7ccb">IDirectXVideoDecoder::BeginFrame</a> before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
 

 

