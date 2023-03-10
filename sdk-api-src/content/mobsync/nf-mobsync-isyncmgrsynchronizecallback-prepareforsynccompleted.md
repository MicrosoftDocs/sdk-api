---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.PrepareForSyncCompleted
title: ISyncMgrSynchronizeCallback::PrepareForSyncCompleted (mobsync.h)
description: Called by a registered handler of an application after the PrepareForSync method is complete.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback interface [Windows Shell]","PrepareForSyncCompleted method","ISyncMgrSynchronizeCallback.PrepareForSyncCompleted","ISyncMgrSynchronizeCallback::PrepareForSyncCompleted","PrepareForSyncCompleted","PrepareForSyncCompleted method [Windows Shell]","PrepareForSyncCompleted method [Windows Shell]","ISyncMgrSynchronizeCallback interface","mobsync/ISyncMgrSynchronizeCallback::PrepareForSyncCompleted","shell.syncmgr_isyncmgrsynchronizecallback_prepareforsynccompleted","syncmgr.isyncmgrsynchronizecallback_prepareforsynccompleted"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_prepareforsynccompleted.htm
tech.root: shell
ms.assetid: 2ba73e09-c01b-44af-8979-8aae450c9c0b
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],PrepareForSyncCompleted method, ISyncMgrSynchronizeCallback.PrepareForSyncCompleted, ISyncMgrSynchronizeCallback::PrepareForSyncCompleted, PrepareForSyncCompleted, PrepareForSyncCompleted method [Windows Shell], PrepareForSyncCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::PrepareForSyncCompleted, shell.syncmgr_isyncmgrsynchronizecallback_prepareforsynccompleted, syncmgr.isyncmgrsynchronizecallback_prepareforsynccompleted
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
 - ISyncMgrSynchronizeCallback::PrepareForSyncCompleted
 - mobsync/ISyncMgrSynchronizeCallback::PrepareForSyncCompleted
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
 - ISyncMgrSynchronizeCallback.PrepareForSyncCompleted
---

# ISyncMgrSynchronizeCallback::PrepareForSyncCompleted


## -description

Called by a registered handler of an application after the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> method is complete.

## -parameters

### -param hr [in]

Type: <b>HRESULT</b>

The return value of the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> method. If S_OK is returned, the synchronization manager calls <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> for the item. If the <b>HRESULT</b> is set to anything other than S_OK, the synchronization manager releases the handler without calling the <b>Synchronize</b> method.

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
The call is completed successfully.

</td>
</tr>
</table>

## -remarks

A registered handler of an application should return as soon as possible from the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> method, and then call this method to notify the synchronization manager  that the registered application is preparing for synchronization.

It is acceptable for the registered handler of an application to call this method before returning from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> method.

The registered handler of an application should not call this method if the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> method returns any value that is different from S_OK.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a>