---
UID: NF:mobsync.ISyncMgrSynchronize.SetItemStatus
title: ISyncMgrSynchronize::SetItemStatus (mobsync.h)
description: Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases:\_between the time the handler has returned from the ISyncMgrSynchronize::PrepareForSync method and called the PrepareForSyncCompleted callback method, or after the handler has returned from the ISyncMgrSynchronize::Synchronize method but has not yet called the SynchronizeCompleted callback method.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","SetItemStatus method","ISyncMgrSynchronize.SetItemStatus","ISyncMgrSynchronize::SetItemStatus","SetItemStatus","SetItemStatus method [Windows Shell]","SetItemStatus method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::SetItemStatus","shell.syncmgr_isyncmgrsynchronize_setitemstatus","syncmgr.isyncmgrsynchronize_setitemstatus"]
old-location: shell\syncmgr_isyncmgrsynchronize_setitemstatus.htm
tech.root: shell
ms.assetid: 311e916c-46a0-4eb2-a5e3-8da417ae7d71
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],SetItemStatus method, ISyncMgrSynchronize.SetItemStatus, ISyncMgrSynchronize::SetItemStatus, SetItemStatus, SetItemStatus method [Windows Shell], SetItemStatus method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::SetItemStatus, shell.syncmgr_isyncmgrsynchronize_setitemstatus, syncmgr.isyncmgrsynchronize_setitemstatus
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
 - ISyncMgrSynchronize::SetItemStatus
 - mobsync/ISyncMgrSynchronize::SetItemStatus
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
 - ISyncMgrSynchronize.SetItemStatus
---

# ISyncMgrSynchronize::SetItemStatus


## -description

Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases: between the time the handler has returned from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> method and called the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted">PrepareForSyncCompleted</a> callback method, or after the handler has returned from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> method but has not yet called the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">SynchronizeCompleted</a> callback method.

## -parameters

### -param pItemID [in]

Type: <b>REFGUID</b>

Identifies the item with changed status.

### -param dwSyncMgrStatus [in]

Type: <b>DWORD</b>

The new status for the specified item taken from the 
<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrstatus">SYNCMGRSTATUS</a> enumeration.

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

Currently, the only <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrstatus">SYNCMGRSTATUS</a> status value supported by the SyncMgr is SYNCMGRSTATUS_SKIPPED. The registered application's handler should skip the item specified in <i>pItemID</i> when it receives this status value.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback">ISyncMgrSynchronize::SetProgressCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted">PrepareForSyncCompleted</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrstatus">SYNCMGRSTATUS</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">SynchronizeCompleted</a>