---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetPresenterNextStep
title: ISyncMgrConflictResolveInfo::GetPresenterNextStep (syncmgr.h)
description: Gets what the presenter wants to do as the next step in the sync manager conflict resolution.
helpviewer_keywords: ["GetPresenterNextStep","GetPresenterNextStep method [Windows Shell]","GetPresenterNextStep method [Windows Shell]","ISyncMgrConflictResolveInfo interface","ISyncMgrConflictResolveInfo interface [Windows Shell]","GetPresenterNextStep method","ISyncMgrConflictResolveInfo.GetPresenterNextStep","ISyncMgrConflictResolveInfo::GetPresenterNextStep","_shell_ISyncMgrConflictResolveInfo_GetPresenterNextStep","shell.ISyncMgrConflictResolveInfo_GetPresenterNextStep","syncmgr/ISyncMgrConflictResolveInfo::GetPresenterNextStep"]
old-location: shell\ISyncMgrConflictResolveInfo_GetPresenterNextStep.htm
tech.root: shell
ms.assetid: 7f263f83-1d7c-40c6-a57c-1334a52cd712
ms.date: 12/05/2018
ms.keywords: GetPresenterNextStep, GetPresenterNextStep method [Windows Shell], GetPresenterNextStep method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetPresenterNextStep method, ISyncMgrConflictResolveInfo.GetPresenterNextStep, ISyncMgrConflictResolveInfo::GetPresenterNextStep, _shell_ISyncMgrConflictResolveInfo_GetPresenterNextStep, shell.ISyncMgrConflictResolveInfo_GetPresenterNextStep, syncmgr/ISyncMgrConflictResolveInfo::GetPresenterNextStep
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
 - ISyncMgrConflictResolveInfo::GetPresenterNextStep
 - syncmgr/ISyncMgrConflictResolveInfo::GetPresenterNextStep
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
 - ISyncMgrConflictResolveInfo.GetPresenterNextStep
---

# ISyncMgrConflictResolveInfo::GetPresenterNextStep


## -description

Gets what the presenter wants to do as the next step in the sync manager conflict resolution.

## -parameters

### -param pnPresenterNextStep [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_next_step">SYNCMGR_PRESENTER_NEXT_STEP</a>*</b>

When this method returns, contains a pointer to the next step in conflict resolution. One of the members of the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_next_step">SYNCMGR_PRESENTER_NEXT_STEP</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setpresenternextstep">ISyncMgrConflictResolveInfo::SetPresenterNextStep</a>