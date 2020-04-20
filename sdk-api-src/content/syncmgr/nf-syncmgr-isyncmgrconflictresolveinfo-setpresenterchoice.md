---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.SetPresenterChoice
title: ISyncMgrConflictResolveInfo::SetPresenterChoice (syncmgr.h)
description: Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set.helpviewer_keywords: ["ISyncMgrConflictResolveInfo interface [Windows Shell]","SetPresenterChoice method","ISyncMgrConflictResolveInfo.SetPresenterChoice","ISyncMgrConflictResolveInfo::SetPresenterChoice","SetPresenterChoice","SetPresenterChoice method [Windows Shell]","SetPresenterChoice method [Windows Shell]","ISyncMgrConflictResolveInfo interface","_shell_ISyncMgrConflictResolveInfo_SetPresenterChoice","shell.ISyncMgrConflictResolveInfo_SetPresenterChoice","syncmgr/ISyncMgrConflictResolveInfo::SetPresenterChoice"]
old-location: shell\ISyncMgrConflictResolveInfo_SetPresenterChoice.htm
tech.root: shell
ms.assetid: 5f4bfe69-1ff3-4d21-9c27-f5d8ecfc8371
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictResolveInfo interface [Windows Shell],SetPresenterChoice method, ISyncMgrConflictResolveInfo.SetPresenterChoice, ISyncMgrConflictResolveInfo::SetPresenterChoice, SetPresenterChoice, SetPresenterChoice method [Windows Shell], SetPresenterChoice method [Windows Shell],ISyncMgrConflictResolveInfo interface, _shell_ISyncMgrConflictResolveInfo_SetPresenterChoice, shell.ISyncMgrConflictResolveInfo_SetPresenterChoice, syncmgr/ISyncMgrConflictResolveInfo::SetPresenterChoice
f1_keywords:
- syncmgr/ISyncMgrConflictResolveInfo.SetPresenterChoice
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
- ISyncMgrConflictResolveInfo.SetPresenterChoice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictResolveInfo::SetPresenterChoice


## -description


Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set.


## -parameters




### -param nPresenterChoice [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_choice">SYNCMGR_PRESENTER_CHOICE</a></b>

The choice that was made about the conflict resolution. One of the members of the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_presenter_choice">SYNCMGR_PRESENTER_CHOICE</a> enumeration.


### -param fApplyToAll [in]

Type: <b>BOOL</b>

If <b>TRUE</b>, then apply the given choice to all subsequent conflicts in the set. In this case, <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setitemchoices">ISyncMgrConflictResolveInfo::SetItemChoices</a> must also be called.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getpresenterchoice">ISyncMgrConflictResolveInfo::GetPresenterChoice</a>
 

 

