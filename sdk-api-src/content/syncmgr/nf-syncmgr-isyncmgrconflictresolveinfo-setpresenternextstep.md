---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.SetPresenterNextStep
title: ISyncMgrConflictResolveInfo::SetPresenterNextStep (syncmgr.h)
description: Sets what the presenter wants to do as the next step in the sync manager conflict resolution.
helpviewer_keywords: ["ISyncMgrConflictResolveInfo interface [Windows Shell]","SetPresenterNextStep method","ISyncMgrConflictResolveInfo.SetPresenterNextStep","ISyncMgrConflictResolveInfo::SetPresenterNextStep","SetPresenterNextStep","SetPresenterNextStep method [Windows Shell]","SetPresenterNextStep method [Windows Shell]","ISyncMgrConflictResolveInfo interface","_shell_ISyncMgrConflictResolveInfo_SetPresenterNextStep","shell.ISyncMgrConflictResolveInfo_SetPresenterNextStep","syncmgr/ISyncMgrConflictResolveInfo::SetPresenterNextStep"]
old-location: shell\ISyncMgrConflictResolveInfo_SetPresenterNextStep.htm
tech.root: shell
ms.assetid: a56ca252-89e5-4ad0-bc9a-f8c7b70bd536
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictResolveInfo interface [Windows Shell],SetPresenterNextStep method, ISyncMgrConflictResolveInfo.SetPresenterNextStep, ISyncMgrConflictResolveInfo::SetPresenterNextStep, SetPresenterNextStep, SetPresenterNextStep method [Windows Shell], SetPresenterNextStep method [Windows Shell],ISyncMgrConflictResolveInfo interface, _shell_ISyncMgrConflictResolveInfo_SetPresenterNextStep, shell.ISyncMgrConflictResolveInfo_SetPresenterNextStep, syncmgr/ISyncMgrConflictResolveInfo::SetPresenterNextStep
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
 - ISyncMgrConflictResolveInfo::SetPresenterNextStep
 - syncmgr/ISyncMgrConflictResolveInfo::SetPresenterNextStep
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
 - ISyncMgrConflictResolveInfo.SetPresenterNextStep
---

# ISyncMgrConflictResolveInfo::SetPresenterNextStep


## -description

Sets what the presenter wants to do as the next step in the sync manager conflict resolution.

## -parameters

### -param nPresenterNextStep [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_next_step">SYNCMGR_PRESENTER_NEXT_STEP</a></b>

The next step in the conflict resolution. One of the members of the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_next_step">SYNCMGR_PRESENTER_NEXT_STEP</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getpresenternextstep">ISyncMgrConflictResolveInfo::GetPresenterNextStep</a>