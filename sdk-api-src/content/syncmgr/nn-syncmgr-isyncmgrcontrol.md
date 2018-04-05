---
UID: NN:syncmgr.ISyncMgrControl
title: ISyncMgrControl
author: windows-driver-content
description: Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.
old-location: shell\ISyncMgrControl.htm
old-project: shell
ms.assetid: 197c4e6f-ffc4-4f19-a5bd-6859eef953c2
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISyncMgrControl, ISyncMgrControl interface [Windows Shell], ISyncMgrControl interface [Windows Shell], described, _shell_ISyncMgrControl, shell.ISyncMgrControl, syncmgr/ISyncMgrControl
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
-	ISyncMgrControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrControl interface


## -description


Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95f332a4-c76c-437f-a756-528cbbb39e2d">ActivateHandler</a>
</td>
<td align="left" width="63%">
Activates or deactivates a handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92a9525c-bf06-4720-a3e2-5352fa693c8e">EnableHandler</a>
</td>
<td align="left" width="63%">
Enables or disables a handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e88fb21-201c-47b9-b341-1a8d9358a455">EnableItem</a>
</td>
<td align="left" width="63%">
Enables or disables a sync item managed by a specified handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">StartHandlerSync</a>
</td>
<td align="left" width="63%">
Initiates the synchronization of all items managed by a particular handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">StartItemSync</a>
</td>
<td align="left" width="63%">
Initiates the synchronization of specified items managed by a particular handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b0d5070-1866-4346-b2bf-93b48a952af6">StartSyncAll</a>
</td>
<td align="left" width="63%">
Synchronizes all items managed by all handlers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a1ba08a-8765-49b5-be71-373af76375f8">StopHandlerSync</a>
</td>
<td align="left" width="63%">
Stops the synchronization of a specified handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd56f26b-caae-4f4d-9a32-fac450e255d0">StopItemSync</a>
</td>
<td align="left" width="63%">
Stops the synchronization of specified items managed by a particular handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6f75833-a1b8-46d0-a339-99e5bf814f7f">StopSyncAll</a>
</td>
<td align="left" width="63%">
Stops the synchronization of all items managed by all handlers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/606df5fb-0c4b-49c7-82ed-28f22927953a">UpdateConflicts</a>
</td>
<td align="left" width="63%">
Informs Sync Center that conflicts have been added for a specific handler or item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72848e6a-eec3-45fc-b599-a5a8da2e1070">UpdateEvents</a>
</td>
<td align="left" width="63%">
Informs Sync Center that events have been added for a specific handler or item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a>
</td>
<td align="left" width="63%">
Instructs Sync Center to reenumerate the items managed by a handler or informs it that properties of the handler have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/752f197e-0dad-4b3d-9f70-352f5f50e9ee">UpdateHandlerCollection</a>
</td>
<td align="left" width="63%">
Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/deb87d2f-74da-450a-a424-505240eadacb">UpdateItem</a>
</td>
<td align="left" width="63%">
Informs Sync Center that properties of a sync item have changed.

</td>
</tr>
</table> 


## -remarks



<b>ISyncMgrControl</b> is implemented by Sync Center. It can be instantiated by an application or handler as the CLSID_SyncMgrControl object, which is implemented as a Component Object Model (COM) local server. As a result, calls to <b>ISyncMgrControl</b> methods could take considerable time. Those calls should not be made on a UI thread.

All methods of this interface queue their requests with Sync Center.

<b>ISyncMgrControl</b> is a replacement for <a href="https://msdn.microsoft.com/993fd482-39e0-4966-ba71-eed7e4b54f72">ISyncMgrSynchronizeInvoke</a>.



