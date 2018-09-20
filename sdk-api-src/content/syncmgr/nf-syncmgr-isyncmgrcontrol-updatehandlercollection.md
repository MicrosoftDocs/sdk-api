---
UID: NF:syncmgr.ISyncMgrControl.UpdateHandlerCollection
title: ISyncMgrControl::UpdateHandlerCollection
author: windows-sdk-content
description: Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed.
old-location: shell\ISyncMgrControl_UpdateHandlerCollection.htm
tech.root: shell
ms.assetid: 752f197e-0dad-4b3d-9f70-352f5f50e9ee
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateHandlerCollection method, ISyncMgrControl.UpdateHandlerCollection, ISyncMgrControl::UpdateHandlerCollection, UpdateHandlerCollection, UpdateHandlerCollection method [Windows Shell], UpdateHandlerCollection method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateHandlerCollection, shell.ISyncMgrControl_UpdateHandlerCollection, syncmgr/ISyncMgrControl::UpdateHandlerCollection
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
 - ISyncMgrControl.UpdateHandlerCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrControl::UpdateHandlerCollection


## -description


Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed.


## -parameters




### -param rclsidCollectionID [in]

Type: <b>REFCLSID</b>

A reference to the handler collection's CLSID.


### -param nControlFlags [in]

Type: <b><a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateHandlerCollection</b> does not return until Sync Center has loaded the specified handler collection and reloaded all handler and item information.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::UpdateHandlerCollection</b> by a handler's procedure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CMyDeviceHandler::MiscProc(...)
{
    ...

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&amp;pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center that a new computer has been added.
        hr = pControl-&gt;UpdateHandlerCollection(CLSID_FRSHandlerCollection,
                                               SYNCMGR_CF_NOWAIT);
        pControl-&gt;Release();
    }

    ...

}
</pre>
</td>
</tr>
</table></span></div>


