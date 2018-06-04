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

# IRecordInfo::RecordDestroy


## -description


Releases the resources and deallocates the memory of the record. 




## -parameters




### -param pvRecord [in]

An instance of the record to be destroyed.


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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/979b0702-3342-4036-8113-c84728436ab6">RecordClear</a> is called to release the resources held by the instance of a record without deallocating memory.

<div class="alert"><b>Note</b>  This method can only be called on records allocated through <a href="https://msdn.microsoft.com/f688623e-c03b-456f-bd51-426049e0eb2b">RecordCreate</a> and <a href="https://msdn.microsoft.com/9cc2a46a-ec92-46a7-8b75-8c36598cc441">RecordCreateCopy</a>. If you allocate the record yourself, you cannot call this method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

