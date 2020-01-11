---
UID: NN:syncmgr.ISyncMgrHandler
title: ISyncMgrHandler (syncmgr.h)
description: Exposes methods that make up the primary interface implemented by a sync handler.
old-location: shell\ISyncMgrHandler.htm
tech.root: shell
ms.assetid: 39579030-1cf5-4e82-a5e7-cb3415903d02
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandler, ISyncMgrHandler interface [Windows Shell], ISyncMgrHandler interface [Windows Shell],described, _shell_ISyncMgrHandler, shell.ISyncMgrHandler, syncmgr/ISyncMgrHandler
f1_keywords:
- syncmgr/ISyncMgrHandler
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
- ISyncMgrHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrHandler interface


## -description


Exposes methods that make up the primary interface implemented by a sync handler. Sync Center creates one instance of the handler through this interface to get properties, enumerate sync items, and modify state. Sync Center creates a separate instance of the handler on a separate thread to perform a synchronization or a UI operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-activate">Activate</a>
</td>
<td align="left" width="63%">
Requests that the handler is activated or deactivated. An active handler can be synchronized; an inactive handler cannot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-enable">Enable</a>
</td>
<td align="left" width="63%">
Requests that an <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-activate">active</a> handler be enabled or disabled. An enabled handler can be synchronized and a disabled handler cannot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets a set of flags describing the handler's defined capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-gethandlerinfo">GetHandlerInfo</a>
</td>
<td align="left" width="63%">
Gets properties that describe the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the display name of the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Creates a specific type of object related to the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getpolicies">GetPolicies</a>
</td>
<td align="left" width="63%">
Gets a set of flags describing the policies set by the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">Synchronize</a>
</td>
<td align="left" width="63%">
Initiates a synchronization of a selection of the handler's sync items.

</td>
</tr>
</table> 


## -remarks



<b>ISyncMgrHandler</b> replaces <a href="https://docs.microsoft.com/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>. Some of the earlier functionality has been streamlined, while some has been moved to other interfaces. See the individual method pages for specific information.



