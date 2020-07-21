---
UID: NN:syncmgr.ISyncMgrEvent
title: ISyncMgrEvent (syncmgr.h)
description: Exposes methods that retrieve data from an event store. An event store allows Sync Center to get an enumerator of all events in the store, as well as to retrieve individual events.
helpviewer_keywords: ["ISyncMgrEvent","ISyncMgrEvent interface [Windows Shell]","ISyncMgrEvent interface [Windows Shell]","described","_shell_ISyncMgrEvent","shell.ISyncMgrEvent","syncmgr/ISyncMgrEvent"]
old-location: shell\ISyncMgrEvent.htm
tech.root: shell
ms.assetid: fb9877fc-016c-472b-9af2-f2470c5c7e3b
ms.date: 12/05/2018
ms.keywords: ISyncMgrEvent, ISyncMgrEvent interface [Windows Shell], ISyncMgrEvent interface [Windows Shell],described, _shell_ISyncMgrEvent, shell.ISyncMgrEvent, syncmgr/ISyncMgrEvent
f1_keywords:
- syncmgr/ISyncMgrEvent
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
- ISyncMgrEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrEvent interface


## -description


Exposes methods that retrieve data from an event store. An event store allows Sync Center to get an enumerator of all events in the store, as well as to retrieve individual events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrEvent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrEvent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Gets a context object that can be used by a handler to display properties or execute a context menu action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the event description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-geteventid">GetEventID</a>
</td>
<td align="left" width="63%">
Gets the event ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets event flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-gethandlerid">GetHandlerID</a>
</td>
<td align="left" width="63%">
Gets the ID of the handler for which the event was logged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getitemid">GetItemID</a>
</td>
<td align="left" width="63%">
Gets the ID of the item for which the event was logged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getlevel">GetLevel</a>
</td>
<td align="left" width="63%">
Gets the log level of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getlinkreference">GetLinkReference</a>
</td>
<td align="left" width="63%">
Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getlinktext">GetLinkText</a>
</td>
<td align="left" width="63%">
Gets the text for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder. The link text is the text that is displayed to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Gets the creation time.

</td>
</tr>
</table> 

