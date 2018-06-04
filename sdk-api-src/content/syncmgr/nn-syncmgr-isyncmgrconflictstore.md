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

# ISyncMgrConflictStore interface


## -description


Exposes methods that allow a handler to provide conflicts that appear in the Conflicts folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrConflictStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86414360-7dc5-4819-8372-0cede07ba41b">BindToConflict</a>
</td>
<td align="left" width="63%">
Binds to a particular conflict specified by IID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b59c679c-7759-4b7a-9a23-f054af99d6a7">EnumConflicts</a>
</td>
<td align="left" width="63%">
Enumerates conflicts scoped to the provided sync handler and sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of conflicts in the store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6fbb322-7bb0-4ad0-bf01-2fe407689fe5">RemoveConflicts</a>
</td>
<td align="left" width="63%">
Deletes a set of conflicts, specified by conflict ID, from the store.

</td>
</tr>
</table> 


## -remarks




        Conflict is provided to enable the user to select a version of a <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> as needed, instead of being forced to pick to complete a sync selection set. The fact that we current display them in the conflict folder is purely secondary. 


                  The conflict store must notify sync center when its contents change. Nothing is assumed to happen to conflicts when methods are called that affect the conflict. This includes when they are resolved.

Sync Center requests a conflict store from a handler by calling <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> with SYNCMGR_OBJECTID_ConflictStore if the mask returned from <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">ISyncMgrHandler::GetCapabilities</a> includes SYNCMGR_HCM_CONFLICT_STORE. The handler can also provide an event store filtered by item by setting the SYNCMGR_ICM_CONFLICT_STORE flag in the mask returned from <a href="https://msdn.microsoft.com/6cb98b83-cf17-451c-ba29-700408f474c7">ISyncMgrSyncItem::GetCapabilities</a>.

If conflicts are added to the conflict store, the handler (or a related component) should call <a href="https://msdn.microsoft.com/606df5fb-0c4b-49c7-82ed-28f22927953a">ISyncMgrControl::UpdateConflicts</a> so that both the Conflicts folder and conflict counts can be updated.



