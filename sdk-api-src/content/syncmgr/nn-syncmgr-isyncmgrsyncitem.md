---
UID: NN:syncmgr.ISyncMgrSyncItem
title: ISyncMgrSyncItem (syncmgr.h)
description: Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.helpviewer_keywords: ["ISyncMgrSyncItem","ISyncMgrSyncItem interface [Windows Shell]","ISyncMgrSyncItem interface [Windows Shell]","described","_shell_ISyncMgrSyncItem","shell.ISyncMgrSyncItem","syncmgr/ISyncMgrSyncItem"]
old-location: shell\ISyncMgrSyncItem.htm
tech.root: shell
ms.assetid: 322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItem, ISyncMgrSyncItem interface [Windows Shell], ISyncMgrSyncItem interface [Windows Shell],described, _shell_ISyncMgrSyncItem, shell.ISyncMgrSyncItem, syncmgr/ISyncMgrSyncItem
f1_keywords:
- syncmgr/ISyncMgrSyncItem
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
- ISyncMgrSyncItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSyncItem interface


## -description


Exposes methods that act on and retrieve information from a single sync item, allowing handlers to manage sync items as independent objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncItem</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes a sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables the sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets a set of flags describing the item's defined capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getitemid">GetItemID</a>
</td>
<td align="left" width="63%">
Gets the unique ID of a sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getiteminfo">GetItemInfo</a>
</td>
<td align="left" width="63%">
Gets the properties of a sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the UI display name of the sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Creates a specific type of object related to the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getpolicies">GetPolicies</a>
</td>
<td align="left" width="63%">
Gets a set of flags describing the policies set by the item.

</td>
</tr>
</table> 


## -remarks



A sync item typically represents a group of data, for example, a folder that contains several files. By representing this sync item as an interface, the item can be easily managed and implemented as an object. That object maintains the state of the item when the item is accessed.

Representing a sync item as <b>ISyncMgrSyncItem</b> also allows support for a sync item that contains other sync items.



