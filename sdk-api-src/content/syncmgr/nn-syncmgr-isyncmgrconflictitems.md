---
UID: NN:syncmgr.ISyncMgrConflictItems
title: ISyncMgrConflictItems (syncmgr.h)
description: Exposes methods that get conflict item data and item count.
helpviewer_keywords: ["ISyncMgrConflictItems","ISyncMgrConflictItems interface [Windows Shell]","ISyncMgrConflictItems interface [Windows Shell]","described","_shell_ISyncMgrConflictItems","shell.ISyncMgrConflictItems","syncmgr/ISyncMgrConflictItems"]
old-location: shell\ISyncMgrConflictItems.htm
tech.root: shell
ms.assetid: 1dea310d-137b-4180-99c9-e40cd4fa3a98
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictItems, ISyncMgrConflictItems interface [Windows Shell], ISyncMgrConflictItems interface [Windows Shell],described, _shell_ISyncMgrConflictItems, shell.ISyncMgrConflictItems, syncmgr/ISyncMgrConflictItems
f1_keywords:
- syncmgr/ISyncMgrConflictItems
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
- ISyncMgrConflictItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictItems interface


## -description


Exposes methods that get conflict item data and item count.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictItems</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflictItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictitems-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the conflict item count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictitems-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Gets a specified conflict data item.

</td>
</tr>
</table> 

