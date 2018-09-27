---
UID: NN:syncmgr.ISyncMgrEventStore
title: ISyncMgrEventStore
author: windows-sdk-content
description: Exposes methods that allow a handler to provide its own event store and manage its own sync events, instead of using the default Sync Center event store. These events are displayed in the Sync Results folder.
old-location: shell\ISyncMgrEventStore.htm
tech.root: shell
ms.assetid: 218875bf-be6b-4ca5-8904-81c81c7fbf70
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ISyncMgrEventStore, ISyncMgrEventStore interface [Windows Shell], ISyncMgrEventStore interface [Windows Shell],described, _shell_ISyncMgrEventStore, shell.ISyncMgrEventStore, syncmgr/ISyncMgrEventStore
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
 - ISyncMgrEventStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrEventStore interface


## -description


Exposes methods that allow a handler to provide its own event store and manage its own sync events, instead of using the default Sync Center event store. These events are displayed in the Sync Results folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrEventStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrEventStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrEventStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6800ac62-1fd5-43a4-bd37-831449274a7b">GetEvent</a>
</td>
<td align="left" width="63%">
Gets a specified event object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e8482ed-3cdc-49a3-ad65-237f163e440d">GetEventCount</a>
</td>
<td align="left" width="63%">
Gets the event count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b634811-cb6d-47b2-b534-1baea23a5297">GetEventEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator for a handler's events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08d01b6f-1e1f-4f03-9595-f374805ae734">RemoveEvent</a>
</td>
<td align="left" width="63%">
Removes events, as specified.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Sync Center provides a default event store that handlers can use to report events, which are then displayed in the Sync Results folder. If a component already logs events, it might be more convenient for it to provide its own event store that enumerates events for that handler. The event store in that case would simply translate the event as logged by the component into a form that can be used by Sync Center.

Sync Center requests an event store from a handler by first examining the mask returned by <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">ISyncMgrHandler::GetCapabilities</a> for the SYNCMGR_HCM_EVENT_STORE flag. If that value is present, Sync Center calls <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> with the SYNCMGR_OBJECTID_EventStore value. The handler can also provide an event store filtered by item by setting the SYNCMGR_ICM_EVENT_STORE flag in the mask returned from <a href="https://msdn.microsoft.com/6cb98b83-cf17-451c-ba29-700408f474c7">ISyncMgrSyncItem::GetCapabilities</a>.

If events are added to the event store, the handler (or a related component) should call <a href="https://msdn.microsoft.com/72848e6a-eec3-45fc-b599-a5a8da2e1070">ISyncMgrControl::UpdateEvents</a> so that the Sync Results folder and the error counts can be updated.



