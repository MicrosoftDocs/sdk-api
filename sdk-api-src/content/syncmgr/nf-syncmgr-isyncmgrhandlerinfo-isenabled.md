---
UID: NF:syncmgr.ISyncMgrHandlerInfo.IsEnabled
title: ISyncMgrHandlerInfo::IsEnabled
author: windows-driver-content
description: Gets a value that indicates whether the handler is enabled.
old-location: shell\ISyncMgrHandlerInfo_IsEnabled.htm
old-project: shell
ms.assetid: 1485ae25-20b8-4ee9-a30d-247f719047cd
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ISyncMgrHandlerInfo interface [Windows Shell],IsEnabled method, ISyncMgrHandlerInfo.IsEnabled, ISyncMgrHandlerInfo::IsEnabled, IsEnabled, IsEnabled method [Windows Shell], IsEnabled method [Windows Shell],ISyncMgrHandlerInfo interface, _shell_ISyncMgrHandlerInfo_IsEnabled, shell.ISyncMgrHandlerInfo_IsEnabled, syncmgr/ISyncMgrHandlerInfo::IsEnabled
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
-	ISyncMgrHandlerInfo.IsEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandlerInfo::IsEnabled


## -description


Gets a value that indicates whether the handler is enabled.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the handler is enabled; otherwise, S_FALSE.
                    
                    

If the handler wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the handler's enabled state to the last known value and enables or disables the associated tasks as appropriate.

If either the SYNCMGR_HCM_QUERY_BEFORE_ENABLE or SYNCMGR_HCM_QUERY_BEFORE_DISABLE flag is set in the mask returned from <a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>, the handler must manage its own enabled state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.




## -remarks



If a handler is disabled, neither it nor any of its items will be synchronized by Sync Center. Also, many of the possible actions available to a handler—such as Sync—are removed or disabled in the Sync Center folder UI.

This value is available in the folder UI as the System.Sync.Enabled (PKEY_Sync_Enabled) property.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples




        	The following example shows an implementation of this method that calls a private class function to retrieve the enabled state.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::IsEnabled()
{
    // Return a previously-calculated value.
    return (_fIsEnabled ? S_OK : S_FALSE);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a>



<a href="https://msdn.microsoft.com/29cded59-d0f3-4678-9601-4931687b48e4">ISyncMgrHandlerInfo</a>
 

 

