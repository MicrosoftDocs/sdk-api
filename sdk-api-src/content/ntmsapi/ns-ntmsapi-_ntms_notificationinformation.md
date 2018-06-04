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

# _NTMS_NOTIFICATIONINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_NOTIFICATIONINFORMATION</b> structure defines an object and operation that occurred in the RSM database.


## -struct-fields




### -field dwOperation

Operation that occurred on the object. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_INSERT"></a><a id="ntms_obj_insert"></a><dl>
<dt><b>NTMS_OBJ_INSERT</b></dt>
</dl>
</td>
<td width="60%">
New object was inserted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_DELETE"></a><a id="ntms_obj_delete"></a><dl>
<dt><b>NTMS_OBJ_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Object was deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_UPDATE"></a><a id="ntms_obj_update"></a><dl>
<dt><b>NTMS_OBJ_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Object was updated.

</td>
</tr>
</table>
 


### -field ObjectId

Object Identifier.


## -see-also




<a href="https://msdn.microsoft.com/ecb39bac-f062-4835-bbae-f9f643ffde9b">WaitForNtmsNotification</a>
 

 

