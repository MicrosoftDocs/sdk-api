---
UID: NN:syncmgr.ISyncMgrHandlerInfo
title: ISyncMgrHandlerInfo
author: windows-sdk-content
description: Exposes methods that allow a handler to provide property and state information to Sync Center.
old-location: shell\ISyncMgrHandlerInfo.htm
old-project: shell
ms.assetid: 29cded59-d0f3-4678-9601-4931687b48e4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISyncMgrHandlerInfo, ISyncMgrHandlerInfo interface [Windows Shell], ISyncMgrHandlerInfo interface [Windows Shell],described, _shell_ISyncMgrHandlerInfo, shell.ISyncMgrHandlerInfo, syncmgr/ISyncMgrHandlerInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrHandlerInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandlerInfo interface


## -description


Exposes methods that allow a handler to provide property and state information to Sync Center.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrHandlerInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrHandlerInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrHandlerInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/755d3038-934f-42b7-a807-7037fa0ea21e">GetComment</a>
</td>
<td align="left" width="63%">
Gets a string that contains commentary regarding the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12b670e1-2da1-4a67-bff0-6945b13c3335">GetLastSyncTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the handler was last synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Gets the handler type for Sync Center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1a30aad-bd8e-4375-a914-3010b86d83d9">GetTypeLabel</a>
</td>
<td align="left" width="63%">
Gets a label for the handler type. This typically provides the model of the device or an equivalent handler-specific identity string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bcb06ba-a94a-4a18-a284-48be19ec4b44">IsActive</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the handler can be synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b51a32e7-962b-44f6-8508-26f819be483a">IsConnected</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the handler—typically some type of external device—is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450992">IsEnabled</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the handler is enabled.

</td>
</tr>
</table> 


## -remarks



Handlers should always implement this interface, generally on the same object that implements <a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a>. By implementing <b>ISyncMgrHandlerInfo</b>, the set of properties can be changed without requiring the handler to be recompiled. It also provides type-safe access to the properties.



