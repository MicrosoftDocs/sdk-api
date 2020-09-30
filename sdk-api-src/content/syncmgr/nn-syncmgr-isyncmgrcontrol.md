---
UID: NN:syncmgr.ISyncMgrControl
title: ISyncMgrControl (syncmgr.h)
description: Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.
helpviewer_keywords: ["ISyncMgrControl","ISyncMgrControl interface [Windows Shell]","ISyncMgrControl interface [Windows Shell]","described","_shell_ISyncMgrControl","shell.ISyncMgrControl","syncmgr/ISyncMgrControl"]
old-location: shell\ISyncMgrControl.htm
tech.root: shell
ms.assetid: 197c4e6f-ffc4-4f19-a5bd-6859eef953c2
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl, ISyncMgrControl interface [Windows Shell], ISyncMgrControl interface [Windows Shell],described, _shell_ISyncMgrControl, shell.ISyncMgrControl, syncmgr/ISyncMgrControl
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrControl
 - syncmgr/ISyncMgrControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrControl
---

# ISyncMgrControl interface


## -description

Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrControl</b> also has these types of members:
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
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-activatehandler">ActivateHandler</a>
</td>
<td align="left" width="63%">
Activates or deactivates a handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-enablehandler">EnableHandler</a>
</td>
<td align="left" width="63%">
Enables or disables a handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-enableitem">EnableItem</a>
</td>
<td align="left" width="63%">
Enables or disables a sync item managed by a specified handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">StartHandlerSync</a>
</td>
<td align="left" width="63%">
Initiates the synchronization of all items managed by a particular handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">StartItemSync</a>
</td>
<td align="left" width="63%">
Initiates the synchronization of specified items managed by a particular handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startsyncall">StartSyncAll</a>
</td>
<td align="left" width="63%">
Synchronizes all items managed by all handlers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-stophandlersync">StopHandlerSync</a>
</td>
<td align="left" width="63%">
Stops the synchronization of a specified handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-stopitemsync">StopItemSync</a>
</td>
<td align="left" width="63%">
Stops the synchronization of specified items managed by a particular handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-stopsyncall">StopSyncAll</a>
</td>
<td align="left" width="63%">
Stops the synchronization of all items managed by all handlers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateconflicts">UpdateConflicts</a>
</td>
<td align="left" width="63%">
Informs Sync Center that conflicts have been added for a specific handler or item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateevents">UpdateEvents</a>
</td>
<td align="left" width="63%">
Informs Sync Center that events have been added for a specific handler or item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a>
</td>
<td align="left" width="63%">
Instructs Sync Center to reenumerate the items managed by a handler or informs it that properties of the handler have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandlercollection">UpdateHandlerCollection</a>
</td>
<td align="left" width="63%">
Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateitem">UpdateItem</a>
</td>
<td align="left" width="63%">
Informs Sync Center that properties of a sync item have changed.

</td>
</tr>
</table>

## -remarks

<b>ISyncMgrControl</b> is implemented by Sync Center. It can be instantiated by an application or handler as the CLSID_SyncMgrControl object, which is implemented as a Component Object Model (COM) local server. As a result, calls to <b>ISyncMgrControl</b> methods could take considerable time. Those calls should not be made on a UI thread.

All methods of this interface queue their requests with Sync Center.

<b>ISyncMgrControl</b> is a replacement for <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizeinvoke">ISyncMgrSynchronizeInvoke</a>.