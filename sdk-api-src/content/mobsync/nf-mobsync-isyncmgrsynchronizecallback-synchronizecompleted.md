---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.SynchronizeCompleted
title: ISyncMgrSynchronizeCallback::SynchronizeCompleted (mobsync.h)
description: Called by an application when its Synchronize method is complete.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback interface [Windows Shell]","SynchronizeCompleted method","ISyncMgrSynchronizeCallback.SynchronizeCompleted","ISyncMgrSynchronizeCallback::SynchronizeCompleted","SynchronizeCompleted","SynchronizeCompleted method [Windows Shell]","SynchronizeCompleted method [Windows Shell]","ISyncMgrSynchronizeCallback interface","mobsync/ISyncMgrSynchronizeCallback::SynchronizeCompleted","shell.syncmgr_isyncmgrsynchronizecallback_synchronizecompleted","syncmgr.isyncmgrsynchronizecallback_synchronizecompleted"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_synchronizecompleted.htm
tech.root: shell
ms.assetid: df0f0e20-6b84-4ff1-badb-40006a4b8e2c
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],SynchronizeCompleted method, ISyncMgrSynchronizeCallback.SynchronizeCompleted, ISyncMgrSynchronizeCallback::SynchronizeCompleted, SynchronizeCompleted, SynchronizeCompleted method [Windows Shell], SynchronizeCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::SynchronizeCompleted, shell.syncmgr_isyncmgrsynchronizecallback_synchronizecompleted, syncmgr.isyncmgrsynchronizecallback_synchronizecompleted
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
 - ISyncMgrSynchronizeCallback::SynchronizeCompleted
 - mobsync/ISyncMgrSynchronizeCallback::SynchronizeCompleted
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
 - ISyncMgrSynchronizeCallback.SynchronizeCompleted
---

# ISyncMgrSynchronizeCallback::SynchronizeCompleted


## -description

Called by an application when its <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> method is complete.

## -parameters

### -param hr [in]

Type: <b>HRESULT</b>

The returned result from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> method.

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

A registered handler of an application should return from the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> method as soon as possible, and then call this method to notify the synchronization manager that the synchronization process is complete.

It is acceptable for a registered handler of an application to call this method before returning from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> method.

However, the registered handler of an application should not call this method if the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> method returns any value that is different from S_OK.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a>