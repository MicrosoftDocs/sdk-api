---
UID: NF:winsync.ISyncCallback.OnConflict
title: ISyncCallback::OnConflict
author: windows-sdk-content
description: Occurs when a conflict is detected when the concurrency conflict resolution policy is set to CRP_NONE.
old-location: winsync\isynccallback_onconflict.htm
tech.root: winsync
ms.assetid: 439f2a73-b36c-4604-b739-9f9b68275ac5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnConflict method, ISyncCallback.OnConflict, ISyncCallback::OnConflict, OnConflict, OnConflict method [Windows Sync], OnConflict method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onconflict, winsync/ISyncCallback::OnConflict
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
 - ISyncCallback.OnConflict
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncCallback::OnConflict


## -description


Occurs when a conflict is detected when the concurrency conflict resolution policy is set to <a href="https://msdn.microsoft.com/4c2f7237-32ac-4f2d-bf6a-7959bc5d40d4">CRP_NONE</a>.


## -parameters




### -param pConflict [in]

Information about the conflict. This includes metadata and item data for the two changes that are in conflict.


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
<dt><b>Application-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



This notification can be used by an application to perform custom conflict resolution for concurrency conflicts. To accomplish this, the application inspects and processes the contents of <i>pConflict</i>, and then sets the resolution action for the conflict by calling <a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict::SetResolveActionForChange</a> before it returns from this method.




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>



<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/4fdb7123-d8c8-4ed7-9009-0e772252bbb7">SYNC_FULL_ENUMERATION_ACTION Enumeration</a>
 

 

