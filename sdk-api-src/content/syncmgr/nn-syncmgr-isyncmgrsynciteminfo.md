---
UID: NN:syncmgr.ISyncMgrSyncItemInfo
title: ISyncMgrSyncItemInfo
author: windows-driver-content
description: Exposes methods that provide property and state information for a single sync item.
old-location: shell\ISyncMgrSyncItemInfo.htm
old-project: shell
ms.assetid: b98d216e-f23f-45f3-b42d-e5aa2e540265
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISyncMgrSyncItemInfo, ISyncMgrSyncItemInfo interface [Windows Shell], ISyncMgrSyncItemInfo interface [Windows Shell],described, _shell_ISyncMgrSyncItemInfo, shell.ISyncMgrSyncItemInfo, syncmgr/ISyncMgrSyncItemInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrSyncItemInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItemInfo interface


## -description


Exposes methods that provide property and state information for a single sync item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncItemInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSyncItemInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSyncItemInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3959784b-2926-43fd-b8e5-bb1884e5d321">GetComment</a>
</td>
<td align="left" width="63%">
Gets a string that contains commentary regarding the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce6690fc-bc1b-4177-ad4a-76c51d36e908">GetLastSyncTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the item was last synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f93e929f-c25b-4511-9478-57686f9e205b">GetTypeLabel</a>
</td>
<td align="left" width="63%">
Gets a label for the item type. This typically provides the model of the device or an equivalent item-specific identity string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ecfdba-87fb-4b73-8dac-0279f3f140fc">IsConnected</a>
</td>
<td align="left" width="63%">
Generates a value that indicates whether the item—typically some type of external device—is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450992">IsEnabled</a>
</td>
<td align="left" width="63%">
Generates a value that indicates whether the item is enabled.

</td>
</tr>
</table> 


## -remarks



By representing these properties as an interface, the set of properties can be changed later without recompiling the handler. The interface also provides type-safe access to the properties.

Items should always implement this interface, usually on the same object that implements <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a>.



