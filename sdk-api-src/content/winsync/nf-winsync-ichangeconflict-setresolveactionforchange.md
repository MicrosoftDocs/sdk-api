---
UID: NF:winsync.IChangeConflict.SetResolveActionForChange
title: IChangeConflict::SetResolveActionForChange
author: windows-sdk-content
description: Sets a conflict resolution action for the conflict.
old-location: winsync\ichangeconflict_setresolveactionforchange.htm
tech.root: winsync
ms.assetid: f1a26c85-a00d-408e-96ea-5849c6bb99ff
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IChangeConflict interface [Windows Sync],SetResolveActionForChange method, IChangeConflict.SetResolveActionForChange, IChangeConflict::SetResolveActionForChange, SetResolveActionForChange, SetResolveActionForChange method [Windows Sync], SetResolveActionForChange method [Windows Sync],IChangeConflict interface, winsync.ichangeconflict_setresolveactionforchange, winsync/IChangeConflict::SetResolveActionForChange
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeConflict.SetResolveActionForChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- IChangeConflict.SetResolveActionForChange
: 
---

# IChangeConflict::SetResolveActionForChange


## -description


Sets a conflict resolution action for the conflict.


## -parameters




### -param resolveAction [in]

The conflict resolution action for the conflict.


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
An internal error has occurred.

</td>
</tr>
</table>
 




## -remarks



By setting this action in an event handler for <a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">ISyncCallback::OnConflict</a>, the event handler specifies how a change applier should handle the conflict.




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>



<a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">ISyncCallback::OnConflict Method</a>



<a href="https://msdn.microsoft.com/6549eee1-6bf4-46b0-97d1-bb2c0f1b59a4">SYNC RESOLVE ACTION Enumeration</a>
 

 

