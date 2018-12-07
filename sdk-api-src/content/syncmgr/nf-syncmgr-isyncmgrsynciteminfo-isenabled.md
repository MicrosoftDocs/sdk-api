---
UID: NF:syncmgr.ISyncMgrSyncItemInfo.IsEnabled
title: ISyncMgrSyncItemInfo::IsEnabled
author: windows-sdk-content
description: Generates a value that indicates whether the item is enabled.
old-location: shell\ISyncMgrSyncItemInfo_IsEnabled.htm
tech.root: shell
ms.assetid: 47383322-3fb6-47aa-9c97-9d432845fd35
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncMgrSyncItemInfo interface [Windows Shell],IsEnabled method, ISyncMgrSyncItemInfo.IsEnabled, ISyncMgrSyncItemInfo::IsEnabled, IsEnabled, IsEnabled method [Windows Shell], IsEnabled method [Windows Shell],ISyncMgrSyncItemInfo interface, _shell_ISyncMgrSyncItemInfo_IsEnabled, shell.ISyncMgrSyncItemInfo_IsEnabled, syncmgr/ISyncMgrSyncItemInfo::IsEnabled
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
 - ISyncMgrSyncItemInfo.IsEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncItemInfo::IsEnabled


## -description


Generates a value that indicates whether the item is enabled.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the item is enabled; otherwise, S_FALSE.
                    
                    

If the item wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the item's enabled state to the last known value and enables or disables the associated tasks as appropriate.

If either the SYNCMGR_ICM_QUERY_BEFORE_ENABLE or SYNCMGR_ICM_QUERY_BEFORE_DISABLE flags are set in the mask returned from <a href="https://msdn.microsoft.com/6cb98b83-cf17-451c-ba29-700408f474c7">GetCapabilities</a>, the handler must manage its own enabled state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.




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


