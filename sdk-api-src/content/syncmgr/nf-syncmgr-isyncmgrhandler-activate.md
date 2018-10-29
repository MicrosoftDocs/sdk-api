---
UID: NF:syncmgr.ISyncMgrHandler.Activate
title: ISyncMgrHandler::Activate
author: windows-sdk-content
description: Requests that the handler is activated or deactivated. An active handler can be synchronized; an inactive handler cannot.
old-location: shell\ISyncMgrHandler_Activate.htm
tech.root: shell
ms.assetid: 0061387d-516d-44c5-b511-3236593382a9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Activate, Activate method [Windows Shell], Activate method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],Activate method, ISyncMgrHandler.Activate, ISyncMgrHandler::Activate, _shell_ISyncMgrHandler_Activate, shell.ISyncMgrHandler_Activate, syncmgr/ISyncMgrHandler::Activate
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
 - ISyncMgrHandler.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrHandler::Activate


## -description


Requests that the handler is activated or deactivated. An active handler can be synchronized; an inactive handler cannot.


## -parameters




### -param fActivate [in]

Type: <b>BOOL</b>

<b>TRUE</b> to activate; <b>FALSE</b> to deactivate.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An active handler appears in the Sync Center folder and can be synchronized. An inactive handler appears in the Sync Setup folder and must be activated (which moves it to the Sync Center folder) before it can be synchronized.

The activation state should not be confused with the enabled state. An active handler can be disabled. This means that it is still shown in the Sync Center folder but that it cannot be synchronized.

Sync Center calls this method in the following two instances.
            
                

<ul>
<li>When the user selects the handler in the Sync Setup folder and launches its <b>Setup</b> task. If the handler supports the <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">SYNCMGR_OBJECTID_QueryBeforeActivate</a> object, this method is only called if the UI operation, which consists of a dialog asking the user to confirm whether they want to activate the handler, was successful.</li>
<li>When the user selects the handler in the Sync Center folder and launches its <b>Delete</b> task, but only if the handler has not set the <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_HPM_PREVENT_DEACTIVATE</a> flag. If the handler supports the <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">SYNCMGR_OBJECTID_QueryBeforeDeactivate</a> object, this method is only called if the UI operation was successful.</li>
</ul>
If the <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_HPM_PREVENT_ACTIVATE</a> flag is set in the value retrieved by <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">ISyncMgrHandler::GetCapabilities</a>, a call to this method requesting activation of the handler will fail.

The activation state of an individual handler can be found by calling <a href="https://msdn.microsoft.com/0bcb06ba-a94a-4a18-a284-48be19ec4b44">IsActive</a>.

If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL as shown in the example below.


#### Examples



The following example shows a simple implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::Activate(__in BOOL fActivate)
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



<a href="https://msdn.microsoft.com/66dd853e-0fb0-4736-982a-e0183cb51842">ISyncMgrUIOperation::Run</a>
 

 

