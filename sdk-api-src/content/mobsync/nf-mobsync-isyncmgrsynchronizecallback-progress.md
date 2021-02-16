---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.Progress
title: ISyncMgrSynchronizeCallback::Progress (mobsync.h)
description: Called by a registered application to update the progress information and determine whether an operation should continue.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback interface [Windows Shell]","Progress method","ISyncMgrSynchronizeCallback.Progress","ISyncMgrSynchronizeCallback::Progress","Progress","Progress method [Windows Shell]","Progress method [Windows Shell]","ISyncMgrSynchronizeCallback interface","mobsync/ISyncMgrSynchronizeCallback::Progress","shell.syncmgr_isyncmgrsynchronizecallback_progress","syncmgr.isyncmgrsynchronizecallback_progress"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_progress.htm
tech.root: shell
ms.assetid: 924310aa-e210-476d-b532-f235de943498
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],Progress method, ISyncMgrSynchronizeCallback.Progress, ISyncMgrSynchronizeCallback::Progress, Progress, Progress method [Windows Shell], Progress method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::Progress, shell.syncmgr_isyncmgrsynchronizecallback_progress, syncmgr.isyncmgrsynchronizecallback_progress
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
req.lib: 
req.dll: Mobsync.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSynchronizeCallback::Progress
 - mobsync/ISyncMgrSynchronizeCallback::Progress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeCallback.Progress
---

# ISyncMgrSynchronizeCallback::Progress


## -description

Called by a registered application to update the progress information and determine whether an operation should continue.

## -parameters

### -param ItemID [in]

Type: <b>REFGUID</b>

A reference to the item identifier for an item that is being updated.

### -param pSyncProgressItem [in]

Type: <b>const <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrprogressitem">SYNCMGRPROGRESSITEM</a>*</b>

A pointer to a <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrprogressitem">SYNCMGRPROGRESSITEM</a> structure that contains the updated progress information.

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

Registered applications should call this method to provide normal feedback even when the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is set.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a>



<a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrprogressitem">SYNCMGRPROGRESSITEM</a>