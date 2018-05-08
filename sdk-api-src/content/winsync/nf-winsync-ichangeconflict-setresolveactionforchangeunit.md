---
UID: NF:winsync.IChangeConflict.SetResolveActionForChangeUnit
title: IChangeConflict::SetResolveActionForChangeUnit
author: windows-driver-content
description: Sets a conflict resolution action for the conflicting change unit change.
old-location: winsync\ichangeconflict_setresolveactionforchangeunit.htm
old-project: winsync
ms.assetid: 8594a888-21a1-4cfb-964c-9c670e3a7438
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IChangeConflict interface [Windows Sync],SetResolveActionForChangeUnit method, IChangeConflict.SetResolveActionForChangeUnit, IChangeConflict::SetResolveActionForChangeUnit, SetResolveActionForChangeUnit, SetResolveActionForChangeUnit method [Windows Sync], SetResolveActionForChangeUnit method [Windows Sync],IChangeConflict interface, winsync.ichangeconflict_setresolveactionforchangeunit, winsync/IChangeConflict::SetResolveActionForChangeUnit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IChangeConflict.SetResolveActionForChangeUnit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

