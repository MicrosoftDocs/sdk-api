---
UID: NN:syncmgr.ISyncMgrConflict
title: ISyncMgrConflict (syncmgr.h)
description: Exposes methods that provide information about a conflict retrieved from a conflict store, and allows the conflict to be resolved.
helpviewer_keywords: ["ISyncMgrConflict","ISyncMgrConflict interface [Windows Shell]","ISyncMgrConflict interface [Windows Shell]","described","_shell_ISyncMgrConflict","shell.ISyncMgrConflict","syncmgr/ISyncMgrConflict"]
old-location: shell\ISyncMgrConflict.htm
tech.root: shell
ms.assetid: a5806a83-b470-4617-961d-b768160afc48
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflict, ISyncMgrConflict interface [Windows Shell], ISyncMgrConflict interface [Windows Shell],described, _shell_ISyncMgrConflict, shell.ISyncMgrConflict, syncmgr/ISyncMgrConflict
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
 - ISyncMgrConflict
 - syncmgr/ISyncMgrConflict
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
 - ISyncMgrConflict
---

# ISyncMgrConflict interface


## -description

Exposes methods that provide information about a conflict retrieved from a conflict store, and allows the conflict to be resolved.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflict</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflict</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflict</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflict-getconflictidinfo">GetConflictIdInfo</a>
</td>
<td align="left" width="63%">
Gets information that identifies a conflict within a conflict store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflict-getitemsarray">GetItemsArray</a>
</td>
<td align="left" width="63%">
Retrieves a conflict items array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflict-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets a conflict property, given a property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflict-getresolutionhandler">GetResolutionHandler</a>
</td>
<td align="left" width="63%">
Gets the resolution handler for the conflict.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflict-resolve">Resolve</a>
</td>
<td align="left" width="63%">
Resolves the conflict using its own sync handler, controls UI.

</td>
</tr>
</table>