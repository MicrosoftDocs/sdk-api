---
UID: NF:mobsync.ISyncMgrSynchronize.SetItemStatus
title: ISyncMgrSynchronize::SetItemStatus
author: windows-sdk-content
description: Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases:\_between the time the handler has returned from the ISyncMgrSynchronize::PrepareForSync method and called the PrepareForSyncCompleted callback method, or after the handler has returned from the ISyncMgrSynchronize::Synchronize method but has not yet called the SynchronizeCompleted callback method.
old-location: shell\syncmgr_isyncmgrsynchronize_setitemstatus.htm
old-project: shell
ms.assetid: 311e916c-46a0-4eb2-a5e3-8da417ae7d71
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],SetItemStatus method, ISyncMgrSynchronize.SetItemStatus, ISyncMgrSynchronize::SetItemStatus, SetItemStatus, SetItemStatus method [Windows Shell], SetItemStatus method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::SetItemStatus, shell.syncmgr_isyncmgrsynchronize_setitemstatus, syncmgr.isyncmgrsynchronize_setitemstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYNCMGRSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize.SetItemStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronize::SetItemStatus


## -description


Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases: between the time the handler has returned from the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> method and called the 
<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a> callback method, or after the handler has returned from the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method but has not yet called the <a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a> callback method.


## -parameters




### -param pItemID [in]

Type: <b>REFGUID</b>

Identifies the item with changed status.


### -param dwSyncMgrStatus [in]

Type: <b>DWORD</b>

The new status for the specified item taken from the 
<a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a> enumeration.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values, E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, as well as the following:

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
Status was set.

</td>
</tr>
</table>
 




## -remarks



Currently, the only <a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a> status value supported by the SyncMgr is SYNCMGRSTATUS_SKIPPED. The registered application's handler should skip the item specified in <i>pItemID</i> when it receives this status value.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a>



<a href="https://msdn.microsoft.com/193926e8-824c-4969-9707-e2d95961c242">ISyncMgrSynchronize::SetProgressCallback</a>



<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a>



<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a>



<a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a>



<a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a>
 

 

