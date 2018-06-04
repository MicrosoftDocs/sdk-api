---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISyncMgrHandlerInfo::IsActive


## -description


Gets a value that indicates whether the handler can be synchronized.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the handler is active; otherwise, S_FALSE.
                    
                    

If the handler wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the handler's state to the last known value. If the handler's last known value in that situation was inactive, Sync Center disables the <b>Setup</b> task. If the handler's last known value was active, the <b>Delete</b> task is not disabled.

If either the SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE or SYNCMGR_HCM_QUERY_BEFORE_DEACTIVE flag is set in the mask returned from <a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>, the handler must manage its own activation state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.




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
 

 

