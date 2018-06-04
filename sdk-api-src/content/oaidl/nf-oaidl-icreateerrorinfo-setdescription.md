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

# ICreateErrorInfo::SetDescription


## -description


Sets the textual description of the error.


## -parameters




### -param szDescription [in]

A brief description of the error.


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>
 




## -remarks



The text should be supplied in the language specified by the locale ID (LCID) that was passed to the method raising the error. For more information, see LCID Attribute in <a href="https://msdn.microsoft.com/c4061d23-b6bd-43f4-adf0-5980dae7a059">Type Libraries and the Object Description Language</a>. 



Use of this function is demonstrated in the file Main.cpp of the COM Fundamentals Hello sample.




## -see-also




<a href="https://msdn.microsoft.com/2e7c5ad5-9018-413e-8826-ef752ebf302c">ICreateErrorInfo</a>
 

 

