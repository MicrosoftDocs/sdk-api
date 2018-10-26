---
UID: NF:syncmgr.ISyncMgrControl.EnableHandler
title: ISyncMgrControl::EnableHandler
author: windows-sdk-content
description: Enables or disables a handler.
old-location: shell\ISyncMgrControl_EnableHandler.htm
tech.root: shell
ms.assetid: 92a9525c-bf06-4720-a3e2-5352fa693c8e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: EnableHandler, EnableHandler method [Windows Shell], EnableHandler method [Windows Shell],ISyncMgrControl interface, ISyncMgrControl interface [Windows Shell],EnableHandler method, ISyncMgrControl.EnableHandler, ISyncMgrControl::EnableHandler, _shell_ISyncMgrControl_EnableHandler, shell.ISyncMgrControl_EnableHandler, syncmgr/ISyncMgrControl::EnableHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrControl.EnableHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrControl::EnableHandler


## -description


Enables or disables a handler.


## -parameters




### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.


### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to a window that can be used by the handler to display any necessary UI. This value can be <b>NULL</b>.


### -param nControlFlags [in]

Type: <b><a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the enabling or disabling of the handler should be performed synchronously or asynchronously.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An active handler appears in the Sync Center folder; an inactive handler appears in the Sync Setup folder.

If the specified handler returns <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_QUERY_BEFORE_ENABLE</a> or <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_QUERY_BEFORE_DISABLE</a> in the mask returned from the <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">GetCapabilities</a> method, the user is presented with a confirmation dialog requested before the handler is enabled or disabled. If no query UI is requested or once the user confirms the operation, the handler's <a href="https://msdn.microsoft.com/ea3efba1-9b7c-4f93-aca5-08475a6005a8">Enable</a> method is called.

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>EnableHandler</b> does not return until Sync Center has processed this notification.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::EnableHandler</b> by a handler's procedure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void MiscProc(...)
{
    ...

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&amp;pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center to enable our handler.
        hr = pControl-&gt;EnableHandler(TRUE, 
                                     s_szMySyncHandlerID, 
                                     hwnd,
                                     SYNCMGR_CF_NOWAIT);
        pControl-&gt;Release();
    }

    ...

}
</pre>
</td>
</tr>
</table></span></div>


