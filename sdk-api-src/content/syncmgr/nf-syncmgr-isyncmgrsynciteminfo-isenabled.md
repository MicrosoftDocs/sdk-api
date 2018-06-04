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

# ISyncMgrSyncItemInfo::IsEnabled


## -description


Generates a value that indicates whether the item is enabled.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the item is enabled; otherwise, S_FALSE.
                    
                    

If the item wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the item's enabled state to the last known value and enables or disables the associated tasks as appropriate.

If either the SYNCMGR_ICM_QUERY_BEFORE_ENABLE or SYNCMGR_ICM_QUERY_BEFORE_DISABLE flags are set in the mask returned from <a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>, the handler must manage its own enabled state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.




## -remarks



If an item is disabled, it is not synchronized by Sync Center. Also, many of the possible actions available to an item—such as Sync—are removed or disabled in the UI.

An item can implement a <a href="https://msdn.microsoft.com/12ecfdba-87fb-4b73-8dac-0279f3f140fc">Disconnected</a> state by returning S_FALSE from <b>IsEnabled</b> and setting the SYNCMR_IPM_PREVENT_ENABLE flag in its <a href="https://msdn.microsoft.com/5f4e1a8e-8fa7-48b3-8f20-8b260540ab9c">GetPolicies</a> implementation. This shows the item as disabled and prevents the user from enabling it manually.

The enabled value is available in the folder UI as the System.Sync.Enabled (PKEY_Sync_Enabled) property.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples




        	The following example shows an implementation of this method that calls a private class function to retrieve the enabled state.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::IsEnabled()
{
    // Return a previously-calculated value.
    return (_fIsEnabled ? S_OK : S_FALSE);
}
</pre>
</td>
</tr>
</table></span></div>


