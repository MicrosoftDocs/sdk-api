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

# CreateErrorInfo function


## -description


Creates an instance of a generic error object.


## -parameters




### -param pperrinfo [out]

A system-implemented generic error object.


## -returns



This function can return one of these values.

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
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Could not create the error object.

</td>
</tr>
</table>
 




## -remarks



This function returns a pointer to a generic error object, which you can use with <b>QueryInterface</b> on <a href="https://msdn.microsoft.com/2e7c5ad5-9018-413e-8826-ef752ebf302c">ICreateErrorInfo</a> to set its contents. You can then pass the resulting object to <a href="8EAACFAC-FC37-4EAA-870B-10B99D598D66">SetErrorInfo</a>. The generic error object implements both <b>ICreateErrorInfo</b> and <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/483ca37a-332c-4a0e-9c27-cc6b885a3005">Error-Handling API Functions</a>
 

 

