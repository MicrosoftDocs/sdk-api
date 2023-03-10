---
UID: NF:syncmgr.ISyncMgrConflict.Resolve
title: ISyncMgrConflict::Resolve (syncmgr.h)
description: Resolves the conflict using its own sync handler, controls UI.
helpviewer_keywords: ["ISyncMgrConflict interface [Windows Shell]","Resolve method","ISyncMgrConflict.Resolve","ISyncMgrConflict::Resolve","Resolve","Resolve method [Windows Shell]","Resolve method [Windows Shell]","ISyncMgrConflict interface","_shell_ISyncMgrConflict_Resolve","shell.ISyncMgrConflict_Resolve","syncmgr/ISyncMgrConflict::Resolve"]
old-location: shell\ISyncMgrConflict_Resolve.htm
tech.root: shell
ms.assetid: 9680b96e-9a83-45e1-a2bf-674aff6490ec
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflict interface [Windows Shell],Resolve method, ISyncMgrConflict.Resolve, ISyncMgrConflict::Resolve, Resolve, Resolve method [Windows Shell], Resolve method [Windows Shell],ISyncMgrConflict interface, _shell_ISyncMgrConflict_Resolve, shell.ISyncMgrConflict_Resolve, syncmgr/ISyncMgrConflict::Resolve
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
 - ISyncMgrConflict::Resolve
 - syncmgr/ISyncMgrConflict::Resolve
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
 - ISyncMgrConflict.Resolve
---

# ISyncMgrConflict::Resolve


## -description

Resolves the conflict using its own sync handler, controls UI.

## -parameters

### -param pResolveInfo [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>*</b>

A pointer to a <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Note that the store must tell the sync center if the conflict was removed by calling <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateconflicts">UpdateConflicts</a> after the conflict is resolved. The conflict is assumed to still exist until the store notifies the sync center of changes. The resolution choices for user selection are available through <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>.