---
UID: NN:syncmgr.ISyncMgrResolutionHandler
title: ISyncMgrResolutionHandler
author: windows-driver-content
description: Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.
old-location: shell\ISyncMgrResolutionHandler.htm
old-project: shell
ms.assetid: 5b77217d-5c63-41be-b4df-338714a90fb9
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ISyncMgrResolutionHandler, ISyncMgrResolutionHandler interface [Windows Shell], ISyncMgrResolutionHandler interface [Windows Shell],described, _shell_ISyncMgrResolutionHandler, shell.ISyncMgrResolutionHandler, syncmgr/ISyncMgrResolutionHandler
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
-	ISyncMgrResolutionHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrResolutionHandler interface


## -description


Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.
       


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrResolutionHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrResolutionHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrResolutionHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81be006b-4aa4-42da-ae1b-001ae92a3e9b">KeepItems</a>
</td>
<td align="left" width="63%">
Keeps the Shell items that are passed in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d3e3b01-447c-4f7b-8a63-5bd9084de00a">KeepOther</a>
</td>
<td align="left" width="63%">
Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2327234-4a8d-42b4-aa62-f5c286e3c24b">KeepRecent</a>
</td>
<td align="left" width="63%">
Keeps the more recent copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f178c4d9-0c83-4569-81fe-fe38ac13f0b5">QueryAbilities</a>
</td>
<td align="left" width="63%">
Determines what options the conflict presenter will display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f65f844-efa2-43b9-91f2-c9c0ed4e3a9e">RemoveFromSyncSet</a>
</td>
<td align="left" width="63%">
Deletes the conflict and removes the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>  from synchronization.

</td>
</tr>
</table> 

