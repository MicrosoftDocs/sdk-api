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

# IChangeConflict::SetResolveActionForChangeUnit


## -description


Sets a conflict resolution action for the conflicting change unit change.


## -parameters




### -param pChangeUnit [in]

The change unit for which to set the conflict resolution action.


### -param resolveAction [in]

The conflict resolution action to set for <i>pChangeUnit</i>.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INTERNAL_ERROR </b></dt>
</dl>
</td>
<td width="60%">
When the conflict is an update-delete conflict, or when no conflict exists.

</td>
</tr>
</table>
 




## -remarks



Be aware that setting the conflict resolution action for a change unit on an update-delete conflict is not valid, because this type of conflict must be resolved at the item level.

By setting this action in an event handler for <a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">ISyncCallback::OnConflict</a>, the event handler specifies how the change applier should handle the conflict.




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>



<a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">ISyncCallback::OnConflict Method</a>



<a href="https://msdn.microsoft.com/6549eee1-6bf4-46b0-97d1-bb2c0f1b59a4">SYNC RESOLVE ACTION Enumeration</a>
 

 

