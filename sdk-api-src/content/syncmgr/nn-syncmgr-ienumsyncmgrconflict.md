---
UID: NN:syncmgr.IEnumSyncMgrConflict
title: IEnumSyncMgrConflict (syncmgr.h)
description: Exposes conflict enumeration methods.helpviewer_keywords: ["IEnumSyncMgrConflict","IEnumSyncMgrConflict interface [Windows Shell]","IEnumSyncMgrConflict interface [Windows Shell]","described","_shell_IEnumSyncMgrConflict","shell.IEnumSyncMgrConflict","syncmgr/IEnumSyncMgrConflict"]
old-location: shell\IEnumSyncMgrConflict.htm
tech.root: shell
ms.assetid: 627f39be-5c9d-49a1-af73-210cdbb7940a
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrConflict, IEnumSyncMgrConflict interface [Windows Shell], IEnumSyncMgrConflict interface [Windows Shell],described, _shell_IEnumSyncMgrConflict, shell.IEnumSyncMgrConflict, syncmgr/IEnumSyncMgrConflict
f1_keywords:
- syncmgr/IEnumSyncMgrConflict
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
- IEnumSyncMgrConflict
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSyncMgrConflict interface


## -description


Exposes conflict enumeration methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncMgrConflict</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncMgrConflict</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSyncMgrConflict</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrconflict-clone">Clone</a>
</td>
<td align="left" width="63%">
Not used. Clones an <b>IEnumSyncMgrConflict</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrconflict-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of conflicts from the conflicts store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrconflict-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the current position in the enumeration to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrconflict-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips forward the specified number of conflicts in the enumeration.

</td>
</tr>
</table> 


## -remarks



A conflict store returns a pointer to an <b>IEnumSyncMgrConflict</b> interface from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictstore-enumconflicts">ISyncMgrConflictStore::EnumConflicts</a>.



