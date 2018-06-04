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

# IVssComponent::SetPostRestoreFailureMsg


## -description


The 
<b>SetPostRestoreFailureMsg</b> method is used to create a message describing a failure in processing a 
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event.

Only a writer can call this method, and only during a restore operation.


## -parameters




### -param wszPostRestoreFailureMsg [in]

A caller-allocated <b>NULL</b>-terminated wide character string containing the failure message that describes an error that occurred while processing a 
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully set the failure message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The caller is not in the correct state (either backup or restore) for the operation.

</td>
</tr>
</table>
 




## -remarks



The failure message set by 
<b>SetPostRestoreFailureMsg</b> applies to all files in the component and any nonselectable subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/f7d236e9-bd83-4685-b249-4e5b8ada535a">IVssComponent::GetPostRestoreFailureMsg</a>



<a href="https://msdn.microsoft.com/58c007a8-8414-4e2d-8042-d249a723780a">IVssComponent::GetPreRestoreFailureMsg</a>



<a href="https://msdn.microsoft.com/5b273cba-9878-4494-81ef-af1367f1e0a5">IVssComponent::SetPreRestoreFailureMsg</a>
 

 

