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

# IWMWriter::GetInputFormatCount


## -description



The <b>GetInputFormatCount</b> method retrieves the number of media format types supported by this input on the writer.




## -parameters




### -param dwInputNumber [in]

<b>DWORD</b> containing the input number.


### -param pcFormats [out]

Pointer to a count of formats.


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
The <i>pcFormats</i> parameter is <b>NULL</b>.

OR

<i>dwInputNumber</i> is too large.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/c058de81-a29a-4bcd-a819-3cdef11cae9f">IWMWriter::GetInputFormat</a>



<a href="https://msdn.microsoft.com/482adfc4-d9ed-403d-912b-1a5a70baf04c">To Enumerate Input Formats</a>
 

 

