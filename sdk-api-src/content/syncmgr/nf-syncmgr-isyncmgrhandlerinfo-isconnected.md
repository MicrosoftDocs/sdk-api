---
UID: NF:syncmgr.ISyncMgrHandlerInfo.IsConnected
title: ISyncMgrHandlerInfo::IsConnected method
author: windows-driver-content
description: Gets a value that indicates whether the handler&#8212;typically some type of external device&#8212;is connected.
old-location: shell\ISyncMgrHandlerInfo_IsConnected.htm
old-project: shell
ms.assetid: b51a32e7-962b-44f6-8508-26f819be483a
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ISyncMgrHandlerInfo, ISyncMgrHandlerInfo interface [Windows Shell], IsConnected method, ISyncMgrHandlerInfo::IsConnected, IsConnected method [Windows Shell], IsConnected method [Windows Shell], ISyncMgrHandlerInfo interface, IsConnected,ISyncMgrHandlerInfo.IsConnected, _shell_ISyncMgrHandlerInfo_IsConnected, shell.ISyncMgrHandlerInfo_IsConnected, syncmgr/ISyncMgrHandlerInfo::IsConnected
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
-	ISyncMgrHandlerInfo.IsConnected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandlerInfo::IsConnected method


## -description


Gets a value that indicates whether the handler—typically some type of external device—is connected.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the handler is connected; otherwise, S_FALSE. An error returned by this method will be interpreted as S_OK.




## -remarks



If a handler is disconnected, neither it nor any of its items will be synchronized by Sync Center. Also, many of the possible actions available to a handler—such as Sync—are removed or disabled in the Sync Center folder UI.

This value is available in the folder UI as the System.Sync.Connected (PKEY_Sync_Connected) property.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples




        	The following example shows an implementation of this method that calls a private class function to retrieve the connected state.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::IsConnected()
{
    return (_IsConnected() ? S_OK : S_FALSE);
}
</pre>
</td>
</tr>
</table></span></div>


