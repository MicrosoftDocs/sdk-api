---
UID: NF:syncmgr.ISyncMgrConflictPresenter.PresentConflict
title: ISyncMgrConflictPresenter::PresentConflict (syncmgr.h)
description: Presents the conflict to the user.
helpviewer_keywords: ["ISyncMgrConflictPresenter interface [Windows Shell]","PresentConflict method","ISyncMgrConflictPresenter.PresentConflict","ISyncMgrConflictPresenter::PresentConflict","PresentConflict","PresentConflict method [Windows Shell]","PresentConflict method [Windows Shell]","ISyncMgrConflictPresenter interface","_shell_ISyncMgrConflictPresenter_PresentConflict","shell.ISyncMgrConflictPresenter_PresentConflict","syncmgr/ISyncMgrConflictPresenter::PresentConflict"]
old-location: shell\ISyncMgrConflictPresenter_PresentConflict.htm
tech.root: shell
ms.assetid: 632c0e9c-facd-422e-9467-005c44adc175
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictPresenter interface [Windows Shell],PresentConflict method, ISyncMgrConflictPresenter.PresentConflict, ISyncMgrConflictPresenter::PresentConflict, PresentConflict, PresentConflict method [Windows Shell], PresentConflict method [Windows Shell],ISyncMgrConflictPresenter interface, _shell_ISyncMgrConflictPresenter_PresentConflict, shell.ISyncMgrConflictPresenter_PresentConflict, syncmgr/ISyncMgrConflictPresenter::PresentConflict
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
 - ISyncMgrConflictPresenter::PresentConflict
 - syncmgr/ISyncMgrConflictPresenter::PresentConflict
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
 - ISyncMgrConflictPresenter.PresentConflict
---

# ISyncMgrConflictPresenter::PresentConflict


## -description

Presents the conflict to the user.

## -parameters

### -param pConflict [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a>*</b>

Specifies the conflict. See <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a>.

### -param pResolveInfo [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>*</b>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.