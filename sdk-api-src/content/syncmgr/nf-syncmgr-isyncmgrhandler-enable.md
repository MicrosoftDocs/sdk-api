---
UID: NF:syncmgr.ISyncMgrHandler.Enable
title: ISyncMgrHandler::Enable
author: windows-driver-content
description: Requests that an active handler be enabled or disabled. An enabled handler can be synchronized and a disabled handler cannot.
old-location: shell\ISyncMgrHandler_Enable.htm
old-project: shell
ms.assetid: ea3efba1-9b7c-4f93-aca5-08475a6005a8
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Enable, Enable method [Windows Shell], Enable method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],Enable method, ISyncMgrHandler.Enable, ISyncMgrHandler::Enable, _shell_ISyncMgrHandler_Enable, shell.ISyncMgrHandler_Enable, syncmgr/ISyncMgrHandler::Enable
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrHandler.Enable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandler::Enable


## -description


Requests that an <a href="https://msdn.microsoft.com/library/windows/hardware/dn953453">active</a> handler be enabled or disabled. An enabled handler can be synchronized and a disabled handler cannot.


## -parameters




### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A handler must set the <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_CAN_ENABLE</a> and <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_CAN_DISABLE</a> flags for the <b>Enable</b> and <b>Disable</b> entries to appear on the handler's shortcut menu when the handler is shown in the Sync Center folder. Choosing to enable a handler means that it can be synchronized; choosing to disable a handler means that it cannot.

Sync Center calls this method in the following two instances.
            
                

<ul>
<li>When the user selects the handler in the Sync Center folder and launches its <b>Enable</b> task. If the handler supports the <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">SYNCMGR_OBJECTID_QueryBeforeEnable</a> object, this method is only called if the UI operation was successful.</li>
<li>When the user selects the handler in the Sync Center folder and launches its <b>Disable</b> task. If the handler supports the <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">SYNCMGR_OBJECTID_QueryBeforeDisable</a> object, this method is only called if the UI operation was successful.</li>
</ul>
If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL as shown in the example below.


#### Examples




        	The following example shows a simple implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::Enable(__in BOOL fEnable)
{
    return E_NOTIMPL;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a>



<a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450992">IsEnabled</a>
 

 

