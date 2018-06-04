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

# INSSBuffer::GetMaxLength


## -description



The <b>GetMaxLength</b> method retrieves the maximum size to which a buffer can be set. The maximum value is set when the sample is created. If you are using <a href="https://msdn.microsoft.com/b23b2364-fb36-479f-bf92-76a5bb4722de">IWMWriter::AllocateSample</a>, the size you specify becomes the maximum buffer length. The actual amount of the buffer that is used can be retrieved by calling <a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">INSSBuffer::GetLength</a>.




## -parameters




### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the maximum length, in bytes.


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
The <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The maximum size of the buffer as returned by this method does not affect or reflect the size of any data unit extensions associated with the sample stored in the buffer.




## -see-also




<a href="https://msdn.microsoft.com/f95de189-0449-4b88-aba3-7b19f385c8fe">Data Unit Extensions</a>



<a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">INSSBuffer::GetLength</a>
 

 

