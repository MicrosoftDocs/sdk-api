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

# IMediaBuffer::GetBufferAndLength


## -description



The <code>GetBufferAndLength</code> method retrieves the buffer and the size of the valid data in the buffer.




## -parameters




### -param ppBuffer [out]

Address of a pointer that receives the buffer array. Can be <b>NULL</b> if <i>pcbLength</i> is not <b>NULL</b>.


### -param pcbLength [out]

Pointer to a variable that receives the size of the valid data, in bytes. Can be <b>NULL</b> if <i>ppBuffer</i> is not <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



Either parameter can be <b>NULL</b>, in which case it does not receive a value. At least one parameter must be non-<b>NULL</b>. If both parameters are <b>NULL</b>, the method returns E_POINTER.

The value returned in the <i>pcbLength</i> parameter is the size of the valid data in the buffer, not the buffer's allocated size. To obtain the buffer's allocated size, call the <a href="https://msdn.microsoft.com/9e312d3b-4994-4493-861c-cc0f6f112362">IMediaBuffer::GetMaxLength</a> method.




## -see-also




<a href="https://msdn.microsoft.com/74d72ca6-f899-43fc-bdea-5208d920f314">IMediaBuffer Interface</a>



<a href="https://msdn.microsoft.com/bde7cef8-f43e-4a11-8b77-fed5585d390a">Implementing IMediaBuffer</a>
 

 

