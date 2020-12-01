---
UID: NF:syncmgr.ISyncMgrSyncCallback.CanContinue
title: ISyncMgrSyncCallback::CanContinue (syncmgr.h)
description: Determines whether the synchronization has been canceled.
helpviewer_keywords: ["CanContinue","CanContinue method [Windows Shell]","CanContinue method [Windows Shell]","ISyncMgrSyncCallback interface","ISyncMgrSyncCallback interface [Windows Shell]","CanContinue method","ISyncMgrSyncCallback.CanContinue","ISyncMgrSyncCallback::CanContinue","_shell_ISyncMgrSyncCallback_CanContinue","shell.ISyncMgrSyncCallback_CanContinue","syncmgr/ISyncMgrSyncCallback::CanContinue"]
old-location: shell\ISyncMgrSyncCallback_CanContinue.htm
tech.root: shell
ms.assetid: 02106b6f-4c1c-4bd6-b120-2948b1e6d25c
ms.date: 12/05/2018
ms.keywords: CanContinue, CanContinue method [Windows Shell], CanContinue method [Windows Shell],ISyncMgrSyncCallback interface, ISyncMgrSyncCallback interface [Windows Shell],CanContinue method, ISyncMgrSyncCallback.CanContinue, ISyncMgrSyncCallback::CanContinue, _shell_ISyncMgrSyncCallback_CanContinue, shell.ISyncMgrSyncCallback_CanContinue, syncmgr/ISyncMgrSyncCallback::CanContinue
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSyncCallback::CanContinue
 - syncmgr/ISyncMgrSyncCallback::CanContinue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncCallback.CanContinue
---

# ISyncMgrSyncCallback::CanContinue


## -description

Determines whether the synchronization has been canceled.

## -parameters

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the ID of the item.

## -returns

Type: <b>HRESULT</b>

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>A cancellation has not been requested. The synchronization can continue.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>A cancellation has been requested. The handler should call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress">ISyncMgrSyncCallback::ReportProgress</a>, specifying SYNCMGR_PS_CANCELED in the <i>nStatus</i> parameter.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>The value pointed to by <i>pszItemID</i> is either unknown to Sync Center or is not an item managed by this handler.</td>
</tr>
</table>
 

If <i>pszItemID</i> is <b>NULL</b> or an empty string, the return value depends on whether a cancellation has been requested for the entire handler.

## -remarks

A synchronization can be canceled by the user by clicking the <b>Stop</b> or <b>Stop All</b> task on the context menu or the command module. It can also be canceled when an application calls one of the stop methods of the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> interface.

By implementing this functionality as a separate method, the handler can check for a cancellation without reporting progress.


#### Examples



The following example shows the usage of <b>ISyncMgrSyncCallback::CanContinue</b> by the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">Synchronize</a> method.


```cpp
HRESULT CMyDeviceHandler::Synchronize(...)
{
    ...

    // Start synchronizing the sync items.

    ...

    // If a cancellation has been requested, stop the sync and exit.
    if (pCallback->CanContinue(pszItemID) == S_FALSE)
    {
        // End the sync operation and exit the function.
        hr = pCallback->ReportProgress(pszItemID,
                                       pszCancelMessage,
                                       SYNCMGR_PS_CANCELED,
                                       uCurrentStep,
                                       uMaxStep,
                                       NULL);
    }
    ...
}

```