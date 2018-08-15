---
UID: NF:syncmgr.ISyncMgrControl.UpdateConflicts
title: ISyncMgrControl::UpdateConflicts
author: windows-sdk-content
description: Informs Sync Center that conflicts have been added for a specific handler or item.
old-location: shell\ISyncMgrControl_UpdateConflicts.htm
old-project: shell
ms.assetid: 606df5fb-0c4b-49c7-82ed-28f22927953a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateConflicts method, ISyncMgrControl.UpdateConflicts, ISyncMgrControl::UpdateConflicts, UpdateConflicts, UpdateConflicts method [Windows Shell], UpdateConflicts method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateConflicts, shell.ISyncMgrControl_UpdateConflicts, syncmgr/ISyncMgrControl::UpdateConflicts
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrControl.UpdateConflicts
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrControl::UpdateConflicts


## -description


Informs Sync Center that conflicts have been added for a specific handler or item.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler that manages the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character. This parameter can be <b>NULL</b> if the event occurred on the handler rather than on a specific item.


### -param nControlFlags [in]

Type: <b><a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateConflicts</b> does not return until Sync Center has loaded the specified handler, retrieved the handler's conflict store, and reloaded all conflicts from that store. If the handler is provided by a handler collection, the handler collection is also loaded to reload the handler.


#### Examples



The following example shows the usage of <a href="https://msdn.microsoft.com/72848e6a-eec3-45fc-b599-a5a8da2e1070">ISyncMgrControl::UpdateEvents</a> by a handler's procedure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CMyDeviceHandler::Synchronize(...)
{
    ...
    // Add conflicts to the event store.

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&amp;pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center that we added events to our event store.
        // By passing NULL in pszItemID, we tell Sync Center that the conflict
        // occurred on the handler rather than a specific item.
        hr = pControl-&gt;UpdateConflicts(s_szMyDeviceSyncHandlerID, 
                                       NULL,
                                       SYNCMGR_CF_NOWAIT);
        pControl-&gt;Release();
    }

    ...

}
</pre>
</td>
</tr>
</table></span></div>


