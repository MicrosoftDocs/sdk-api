---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMCodecPrivateData::GetPrivateData


## -description



Retrieves the codec data for the video content based on the output type passed using the <a href="https://msdn.microsoft.com/c906ac2d-b3e0-4ecd-8f0e-3fa1a2a0beea">IWMCodecPrivateData::SetPartialOutputType</a> method.



## -parameters




### -param pbData [out]

Address of the buffer that receives the private data. If you set this to <b>NULL</b>, the size required to hold the private data will be returned in <i>pcbData</i>.


### -param pcbData [in, out]

Pointer to the size of the private data in bytes. If pbData is <b>NULL</b>, the method will set this to the correct value.


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



If you are setting properties on the encoder object, you must finish that configuration before getting the private data. Changing properties invalidates any private data that was previously retrieved. If you change properties after getting the private data, retrieve it again and reset the output type.

You must call this method after providing the codec with the output media type (without the private data appended) by calling <a href="https://msdn.microsoft.com/c906ac2d-b3e0-4ecd-8f0e-3fa1a2a0beea">IWMCodecPrivateData::SetPartialOutputType</a>.

After retrieving the private data, allocate a buffer the size of VIDEOINFOHEADER plus <i>pcbData</i>. Then copy the data from your partial output type to the beginning of the buffer and append the private data. 




## -see-also




<a href="https://msdn.microsoft.com/c1216fd7-7cbd-45cf-b694-a5fd9a972fcd">IWMCodecPrivateData Interface</a>
 

 

