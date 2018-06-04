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

# INSSBuffer::SetLength


## -description



The <b>SetLength</b> method specifies the size of the used portion of the buffer. If you are storing a sample in the buffer, call <a href="https://msdn.microsoft.com/3f9e8408-52ce-48aa-ba85-51bdbbfd8b51">INSSBuffer::GetBuffer</a> to retrieve the address of the buffer. Then copy your data to that address and use this method to set the length of the used portion of the buffer.




## -parameters




### -param dwLength [in]

<b>DWORD</b> containing the size of the used portion, in bytes.


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
<i>dwLength</i> is greater than the buffer size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">INSSBuffer::GetLength</a>
 

 

