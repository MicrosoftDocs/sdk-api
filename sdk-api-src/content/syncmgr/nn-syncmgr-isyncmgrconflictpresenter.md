---
UID: NN:syncmgr.ISyncMgrConflictPresenter
title: ISyncMgrConflictPresenter (syncmgr.h)
description: Exposes a method that presents a conflict to the user.helpviewer_keywords: ["ISyncMgrConflictPresenter","ISyncMgrConflictPresenter interface [Windows Shell]","ISyncMgrConflictPresenter interface [Windows Shell]","described","_shell_ISyncMgrConflictPresenter","shell.ISyncMgrConflictPresenter","syncmgr/ISyncMgrConflictPresenter"]
old-location: shell\ISyncMgrConflictPresenter.htm
tech.root: shell
ms.assetid: ec9a2050-23ad-4478-a705-0a7324e8f84d
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictPresenter, ISyncMgrConflictPresenter interface [Windows Shell], ISyncMgrConflictPresenter interface [Windows Shell],described, _shell_ISyncMgrConflictPresenter, shell.ISyncMgrConflictPresenter, syncmgr/ISyncMgrConflictPresenter
f1_keywords:
- syncmgr/ISyncMgrConflictPresenter
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
- ISyncMgrConflictPresenter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictPresenter interface


## -description


Exposes a method that presents a conflict to the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictPresenter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflictPresenter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictPresenter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictpresenter-presentconflict">PresentConflict</a>
</td>
<td align="left" width="63%">
Presents the conflict to the user.

</td>
</tr>
</table> 

