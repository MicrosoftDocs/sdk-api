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

# IAssemblyName::GetName


## -description


The <b>GetName</b> method returns the name portion of the assembly name.


## -parameters




### -param lpcwBuffer [in, out]

When calling this method, set this parameter to the size of the buffer specified by <i>pwzName</i>. The specify the size in characters and include the null terminator. When the method returns, the value of <i>lpcwBuffer</i> is the size of the name returned. 


### -param pwzName [out]

Pointer to the string value that receives  the name.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
</table>
 




## -remarks



This method is equivalent to using the <a href="https://msdn.microsoft.com/0526fac9-1a3f-403b-b886-a7f833913e18">GetProperty</a> method with the <i>PropertyId</i> set to the <b>ASM_NAME_NAME</b> option of <a href="https://msdn.microsoft.com/5e13e90e-68b0-4842-97de-4f179d4c9ad7">ASM_NAME</a>. In case ASM_NAME_NAME is not set, the size of the buffer returned by <i>lpcwBuffer</i> is  0, and the content of <i>pwzName</i> is undefined.




## -see-also




<a href="https://msdn.microsoft.com/304b8fb3-5d17-4af0-b070-450a40dc5cc9">IAssemblyName</a>
 

 

