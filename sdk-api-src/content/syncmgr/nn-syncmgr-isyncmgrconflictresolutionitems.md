---
UID: NN:syncmgr.ISyncMgrConflictResolutionItems
title: ISyncMgrConflictResolutionItems (syncmgr.h)
description: Exposes methods that get item info and item count.
helpviewer_keywords: ["ISyncMgrConflictResolutionItems","ISyncMgrConflictResolutionItems interface [Windows Shell]","ISyncMgrConflictResolutionItems interface [Windows Shell]","described","_shell_ISyncMgrConflictResolutionItems","shell.ISyncMgrConflictResolutionItems","syncmgr/ISyncMgrConflictResolutionItems"]
old-location: shell\ISyncMgrConflictResolutionItems.htm
tech.root: shell
ms.assetid: 5295ebe5-ec37-4070-80eb-5513b519a0c1
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictResolutionItems, ISyncMgrConflictResolutionItems interface [Windows Shell], ISyncMgrConflictResolutionItems interface [Windows Shell],described, _shell_ISyncMgrConflictResolutionItems, shell.ISyncMgrConflictResolutionItems, syncmgr/ISyncMgrConflictResolutionItems
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
 - ISyncMgrConflictResolutionItems
 - syncmgr/ISyncMgrConflictResolutionItems
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
 - ISyncMgrConflictResolutionItems
---

# ISyncMgrConflictResolutionItems interface


## -description

Exposes methods that get item info and item count.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictResolutionItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflictResolutionItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictResolutionItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolutionitems-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets item count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolutionitems-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Gets result information for a specified item, when successful.

</td>
</tr>
</table>