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

# IITPropList::GetDataSize


## -description


Returns the number of bytes needed to save the property data. 


## -parameters




### -param lpvHeader [in]

Pointer to a buffer containing the header. 


### -param dwHdrSize [in]

Size of the header buffer. 


### -param dwDataSize [out, ref]

Size in bytes. 


## -returns



This method can return one of these values.

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
The size was successfully returned. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvHeader</i> parameter is NULL, or <i>dwHdrSize</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid header buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/09200749-bd1d-4266-895e-29e21525bac2">IITPropList</a>



<a href="https://msdn.microsoft.com/73206149-cbc3-475d-8dc8-bb7547f41173">IITPropList::GetHeaderSize</a>
 

 

