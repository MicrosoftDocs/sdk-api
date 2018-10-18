---
UID: NF:syncmgr.ISyncMgrHandlerInfo.GetLastSyncTime
title: ISyncMgrHandlerInfo::GetLastSyncTime
author: windows-sdk-content
description: Gets the date and time when the handler was last synchronized.
old-location: shell\ISyncMgrHandlerInfo_GetLastSyncTime.htm
tech.root: shell
ms.assetid: 12b670e1-2da1-4a67-bff0-6945b13c3335
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetLastSyncTime, GetLastSyncTime method [Windows Shell], GetLastSyncTime method [Windows Shell],ISyncMgrHandlerInfo interface, ISyncMgrHandlerInfo interface [Windows Shell],GetLastSyncTime method, ISyncMgrHandlerInfo.GetLastSyncTime, ISyncMgrHandlerInfo::GetLastSyncTime, _shell_ISyncMgrHandlerInfo_GetLastSyncTime, shell.ISyncMgrHandlerInfo_GetLastSyncTime, syncmgr/ISyncMgrHandlerInfo::GetLastSyncTime
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
 - ISyncMgrHandlerInfo.GetLastSyncTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrHandlerInfo::GetLastSyncTime


## -description


Gets the date and time when the handler was last synchronized.


## -parameters




### -param pftLastSync [out]

Type: <b>FILETIME*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the date and time information.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>pftLastSync</i> points to the value from the previous synchronization.




## -remarks



This value is not displayed in the folder UI by default, but is available as the System.Sync.DateSynchronized (PKEY_Sync_DateSynchronized) property.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the time and date.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetLastSyncTime(__out FILETIME *pftLastSync)
{
    *pftLastSync = _ftLastSync;
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>


