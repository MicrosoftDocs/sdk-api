---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.Progress
title: ISyncMgrSynchronizeCallback::Progress
author: windows-sdk-content
description: Called by a registered application to update the progress information and determine whether an operation should continue.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_progress.htm
old-project: shell
ms.assetid: 924310aa-e210-476d-b532-f235de943498
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],Progress method, ISyncMgrSynchronizeCallback.Progress, ISyncMgrSynchronizeCallback::Progress, Progress, Progress method [Windows Shell], Progress method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::Progress, shell.syncmgr_isyncmgrsynchronizecallback_progress, syncmgr.isyncmgrsynchronizecallback_progress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mobsync.h
req.include-header: 
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
 - ISyncMgrSynchronizeCallback.Progress
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronizeCallback::Progress


## -description


Called by a registered application to update the progress information and determine whether an operation should continue.


## -parameters




### -param ItemID [in]

Type: <b>REFGUID</b>

A reference to the item identifier for an item that is being updated.


### -param pSyncProgressItem [in]

Type: <b>const <a href="https://msdn.microsoft.com/94ac1206-be5f-467c-ab4a-11f574c406ca">SYNCMGRPROGRESSITEM</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/94ac1206-be5f-467c-ab4a-11f574c406ca">SYNCMGRPROGRESSITEM</a> structure that contains the updated progress information.


## -returns



Type: <b>HRESULT</b>

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
Continues the synchronization.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_SYNCMGR_CANCELITEM</b></dt>
</dl>
</td>
<td width="60%">
Cancels the synchronization on a specified item, as soon as possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_SYNCMGR_CANCELALL</b></dt>
</dl>
</td>
<td width="60%">
Cancels the synchronization on all items that are associated with this application, as soon as possible.

</td>
</tr>
</table>
 




## -remarks



Registered applications should call this method to provide normal feedback even when the <a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is set.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG</a>



<a href="https://msdn.microsoft.com/94ac1206-be5f-467c-ab4a-11f574c406ca">SYNCMGRPROGRESSITEM</a>
 

 

