---
UID: NN:syncmgr.ISyncMgrSyncItemInfo
title: ISyncMgrSyncItemInfo (syncmgr.h)
author: windows-sdk-content
description: Exposes methods that provide property and state information for a single sync item.
old-location: shell\ISyncMgrSyncItemInfo.htm
tech.root: shell
ms.assetid: b98d216e-f23f-45f3-b42d-e5aa2e540265
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItemInfo, ISyncMgrSyncItemInfo interface [Windows Shell], ISyncMgrSyncItemInfo interface [Windows Shell],described, _shell_ISyncMgrSyncItemInfo, shell.ISyncMgrSyncItemInfo, syncmgr/ISyncMgrSyncItemInfo
ms.topic: interface
f1_keywords: 
 - "syncmgr/ISyncMgrSyncItemInfo"
dev_langs:
 - c++
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
 - ISyncMgrSyncItemInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSyncItemInfo interface


## -description


Exposes methods that provide property and state information for a single sync item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncItemInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncItemInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-getcomment">GetComment</a>
</td>
<td align="left" width="63%">
Gets a string that contains commentary regarding the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-getlastsynctime">GetLastSyncTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the item was last synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-gettypelabel">GetTypeLabel</a>
</td>
<td align="left" width="63%">
Gets a label for the item type. This typically provides the model of the device or an equivalent item-specific identity string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-isconnected">IsConnected</a>
</td>
<td align="left" width="63%">
Generates a value that indicates whether the item—typically some type of external device—is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-isenabled">IsEnabled</a>
</td>
<td align="left" width="63%">
Generates a value that indicates whether the item is enabled.

</td>
</tr>
</table> 


## -remarks



By representing these properties as an interface, the set of properties can be changed later without recompiling the handler. The interface also provides type-safe access to the properties.

Items should always implement this interface, usually on the same object that implements <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a>.



