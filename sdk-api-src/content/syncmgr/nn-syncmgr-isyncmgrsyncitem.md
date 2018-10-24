---
UID: NN:syncmgr.ISyncMgrSyncItem
title: ISyncMgrSyncItem
author: windows-sdk-content
description: Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.
old-location: shell\ISyncMgrSyncItem.htm
tech.root: shell
ms.assetid: 322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ISyncMgrSyncItem, ISyncMgrSyncItem interface [Windows Shell], ISyncMgrSyncItem interface [Windows Shell],described, _shell_ISyncMgrSyncItem, shell.ISyncMgrSyncItem, syncmgr/ISyncMgrSyncItem
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
 - ISyncMgrSyncItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncItem interface


## -description


Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSyncItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSyncItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403c01fe-928d-4b9b-a087-6cc68d1aa90a">Delete</a>
</td>
<td align="left" width="63%">
Deletes a sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d73508e-4381-47fe-98ba-ab3ef665cd3e">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables the sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cb98b83-cf17-451c-ba29-700408f474c7">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets a set of flags describing the item's defined capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2add1902-1258-49ed-ad44-35d28d0776c1">GetItemID</a>
</td>
<td align="left" width="63%">
Gets the unique ID of a sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6257d66-36c8-41d6-88f0-99417755582b">GetItemInfo</a>
</td>
<td align="left" width="63%">
Gets the properties of a sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a5f8430-7b5a-4184-acc9-ae4395acf2fa">GetName</a>
</td>
<td align="left" width="63%">
Gets the UI display name of the sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">GetObject</a>
</td>
<td align="left" width="63%">
Creates a specific type of object related to the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f4e1a8e-8fa7-48b3-8f20-8b260540ab9c">GetPolicies</a>
</td>
<td align="left" width="63%">
Gets a set of flags describing the policies set by the item.

</td>
</tr>
</table> 


## -remarks



A sync item typically represents a group of data, for example, a folder that contains several files. By representing this sync item as an interface, the item can be easily managed and implemented as an object. That object maintains the state of the item when the item is accessed.

Representing a sync item as <b>ISyncMgrSyncItem</b> also allows support for a sync item that contains other sync items.



