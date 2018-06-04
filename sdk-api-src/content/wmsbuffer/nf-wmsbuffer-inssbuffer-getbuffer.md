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

# INSSBuffer::GetBuffer


## -description



The <b>GetBuffer</b> method retrieves the location of the buffer controlled by the buffer object. Buffers are used to store samples. When passing samples to the writer, you need the location of the buffer so you can copy your samples into it. When you copy data to the address returned by this call, you must call <a href="https://msdn.microsoft.com/3f0e8d8a-efc7-4f1b-8a42-7907439ed8af">INSSBuffer::SetLength</a> to specify how much of the buffer actually contains data.



When receiving samples from the reader or synchronous reader, retrieve the size of the buffer at the same time as the location by calling <a href="https://msdn.microsoft.com/cb03d006-fbaa-4971-8022-41a7fa29fb87">INSSBuffer::GetBufferAndLength</a>.


## -parameters




### -param ppdwBuffer [out]

Pointer to a pointer to the buffer.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppdwBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/cb03d006-fbaa-4971-8022-41a7fa29fb87">INSSBuffer::GetBufferAndLength</a>
 

 

