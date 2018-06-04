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

# UuidIsNil function


## -description



			An application calls the  
<b>UuidIsNil</b> function to determine whether the specified <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> is a nil-valued <b>UUID</b>.


## -parameters




### -param Uuid


<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to test for nil value.


### -param Status

Returns RPC_S_OK.


## -returns



<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



This function acts as though the application called 
<a href="https://msdn.microsoft.com/ee955482-e786-4478-bbaa-7c574ab1ecc5">UuidCreateNil</a>, and then called the 
<a href="https://msdn.microsoft.com/ff83c66c-1f1f-4582-a93b-d7bb5181deec">UuidEqual</a> to compare the returned nil-value <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to the <b>UUID</b> specified in the <i>Uuid</i> parameter.

Upon completion, one of the following values is returned.

<table>
<tr>
<th>Returned value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The <i>Uuid</i> parameter is a nil-valued <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The <i>Uuid</i> parameter is not a nil-valued <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>
 

 

