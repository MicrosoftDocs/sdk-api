---
UID: NN:syncmgr.ISyncMgrEvent
title: ISyncMgrEvent
author: windows-driver-content
description: Exposes methods that retrieve data from an event store. An event store allows Sync Center to get an enumerator of all events in the store, as well as to retrieve individual events.
old-location: shell\ISyncMgrEvent.htm
old-project: shell
ms.assetid: fb9877fc-016c-472b-9af2-f2470c5c7e3b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ISyncMgrEvent, ISyncMgrEvent interface [Windows Shell], ISyncMgrEvent interface [Windows Shell],described, _shell_ISyncMgrEvent, shell.ISyncMgrEvent, syncmgr/ISyncMgrEvent
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
-	ISyncMgrEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent interface


## -description


Exposes methods that retrieve data from an event store. An event store allows Sync Center to get an enumerator of all events in the store, as well as to retrieve individual events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff545736">GetContext</a>
</td>
<td align="left" width="63%">
Gets a context object that can be used by a handler to display properties or execute a context menu action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the event description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2951a015-b365-468b-a143-1b807885a99a">GetEventID</a>
</td>
<td align="left" width="63%">
Gets the event ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Gets event flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2f3bcbf-f14d-41ce-b4fc-3f491465ce84">GetHandlerID</a>
</td>
<td align="left" width="63%">
Gets the ID of the handler for which the event was logged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/243f84eb-ad0b-44ac-bf61-53bb8b6e5af5">GetItemID</a>
</td>
<td align="left" width="63%">
Gets the ID of the item for which the event was logged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2937dc05-9576-43b4-9fbe-6c151dffcace">GetLevel</a>
</td>
<td align="left" width="63%">
Gets the log level of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de625328-59ba-4574-9b7b-3e8fc643c8ad">GetLinkReference</a>
</td>
<td align="left" width="63%">
Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8a7226b-270e-495e-a43f-8e6a9c7a77df">GetLinkText</a>
</td>
<td align="left" width="63%">
Gets the text for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder. The link text is the text that is displayed to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d533ab62-f6b2-4be9-ac58-98250d99a8c3">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cfe8555-4c63-443a-b3da-e671f8e343d4">GetTime</a>
</td>
<td align="left" width="63%">
Gets the creation time.

</td>
</tr>
</table> 

