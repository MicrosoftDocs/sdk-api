---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetPresenterChoice
title: ISyncMgrConflictResolveInfo::GetPresenterChoice (syncmgr.h)
description: Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set.
helpviewer_keywords: ["GetPresenterChoice","GetPresenterChoice method [Windows Shell]","GetPresenterChoice method [Windows Shell]","ISyncMgrConflictResolveInfo interface","ISyncMgrConflictResolveInfo interface [Windows Shell]","GetPresenterChoice method","ISyncMgrConflictResolveInfo.GetPresenterChoice","ISyncMgrConflictResolveInfo::GetPresenterChoice","_shell_ISyncMgrConflictResolveInfo_GetPresenterChoice","shell.ISyncMgrConflictResolveInfo_GetPresenterChoice","syncmgr/ISyncMgrConflictResolveInfo::GetPresenterChoice"]
old-location: shell\ISyncMgrConflictResolveInfo_GetPresenterChoice.htm
tech.root: shell
ms.assetid: 277eee0e-3f75-4ed1-8df2-75289838d3e5
ms.date: 12/05/2018
ms.keywords: GetPresenterChoice, GetPresenterChoice method [Windows Shell], GetPresenterChoice method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetPresenterChoice method, ISyncMgrConflictResolveInfo.GetPresenterChoice, ISyncMgrConflictResolveInfo::GetPresenterChoice, _shell_ISyncMgrConflictResolveInfo_GetPresenterChoice, shell.ISyncMgrConflictResolveInfo_GetPresenterChoice, syncmgr/ISyncMgrConflictResolveInfo::GetPresenterChoice
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
 - ISyncMgrConflictResolveInfo::GetPresenterChoice
 - syncmgr/ISyncMgrConflictResolveInfo::GetPresenterChoice
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
 - ISyncMgrConflictResolveInfo.GetPresenterChoice
---

# ISyncMgrConflictResolveInfo::GetPresenterChoice


## -description

Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set.

## -parameters

### -param pnPresenterChoice [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_choice">SYNCMGR_PRESENTER_CHOICE</a>*</b>

When this method returns, contains a pointer to the choice that was made about the conflict resolution. One of the members of the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_choice">SYNCMGR_PRESENTER_CHOICE</a> enumeration.

### -param pfApplyToAll [out]

Type: <b>BOOL*</b>

When this method returns, contains a pointer to a flag. If <b>TRUE</b>, then the given choice is to be applied to all subsequent conflicts in the set, and <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoice">ISyncMgrConflictResolveInfo::GetItemChoice</a> and <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoicecount">ISyncMgrConflictResolveInfo::GetItemChoiceCount</a> have information on how to apply this choice. Otherwise <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setpresenterchoice">ISyncMgrConflictResolveInfo::SetPresenterChoice</a>