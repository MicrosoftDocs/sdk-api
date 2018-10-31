---
UID: NF:syncmgr.ISyncMgrHandlerInfo.IsActive
title: ISyncMgrHandlerInfo::IsActive
author: windows-sdk-content
description: Gets a value that indicates whether the handler can be synchronized.
old-location: shell\ISyncMgrHandlerInfo_IsActive.htm
tech.root: shell
ms.assetid: 0bcb06ba-a94a-4a18-a284-48be19ec4b44
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ISyncMgrHandlerInfo interface [Windows Shell],IsActive method, ISyncMgrHandlerInfo.IsActive, ISyncMgrHandlerInfo::IsActive, IsActive, IsActive method [Windows Shell], IsActive method [Windows Shell],ISyncMgrHandlerInfo interface, _shell_ISyncMgrHandlerInfo_IsActive, shell.ISyncMgrHandlerInfo_IsActive, syncmgr/ISyncMgrHandlerInfo::IsActive
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
 - ISyncMgrHandlerInfo.IsActive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrHandlerInfo::IsActive


## -description


Gets a value that indicates whether the handler can be synchronized.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the handler is active; otherwise, S_FALSE.
                    
                    

If the handler wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the handler's state to the last known value. If the handler's last known value in that situation was inactive, Sync Center disables the <b>Setup</b> task. If the handler's last known value was active, the <b>Delete</b> task is not disabled.

If either the SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE or SYNCMGR_HCM_QUERY_BEFORE_DEACTIVE flag is set in the mask returned from <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">GetCapabilities</a>, the handler must manage its own activation state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.




## -remarks



If a handler is not active, it appears in the Sync Setup folder. Handlers in that folder cannot be synchronized. To move a handler to the Sync Center folder, the user selects the <b>Setup</b> task on the handler's shortcut menu or from the command module.

If a handler is active it appears in the main Sync Center folder. A handler that is active can be synchronized either by the user or through the <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a> interface. To move a handler to the Sync Setup folder, the user selects the <b>Delete</b> task on the handler's shortcut menu or on the command module.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the active state.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::IsActive()
{
    // Return a previously-calculated value.
    return (_fIsActive ? S_OK : S_FALSE);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0061387d-516d-44c5-b511-3236593382a9">Activate</a>



<a href="https://msdn.microsoft.com/29cded59-d0f3-4678-9601-4931687b48e4">ISyncMgrHandlerInfo</a>
 

 

