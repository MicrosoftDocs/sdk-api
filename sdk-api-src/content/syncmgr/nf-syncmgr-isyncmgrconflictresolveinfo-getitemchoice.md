---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetItemChoice
title: ISyncMgrConflictResolveInfo::GetItemChoice (syncmgr.h)
description: Gets the index of an item that the user wants to keep.
helpviewer_keywords: ["GetItemChoice","GetItemChoice method [Windows Shell]","GetItemChoice method [Windows Shell]","ISyncMgrConflictResolveInfo interface","ISyncMgrConflictResolveInfo interface [Windows Shell]","GetItemChoice method","ISyncMgrConflictResolveInfo.GetItemChoice","ISyncMgrConflictResolveInfo::GetItemChoice","_shell_ISyncMgrConflictResolveInfo_GetItemChoice","shell.ISyncMgrConflictResolveInfo_GetItemChoice","syncmgr/ISyncMgrConflictResolveInfo::GetItemChoice"]
old-location: shell\ISyncMgrConflictResolveInfo_GetItemChoice.htm
tech.root: shell
ms.assetid: 3c857e53-756b-44c2-b3fa-6d57c21939e7
ms.date: 12/05/2018
ms.keywords: GetItemChoice, GetItemChoice method [Windows Shell], GetItemChoice method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetItemChoice method, ISyncMgrConflictResolveInfo.GetItemChoice, ISyncMgrConflictResolveInfo::GetItemChoice, _shell_ISyncMgrConflictResolveInfo_GetItemChoice, shell.ISyncMgrConflictResolveInfo_GetItemChoice, syncmgr/ISyncMgrConflictResolveInfo::GetItemChoice
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
 - ISyncMgrConflictResolveInfo::GetItemChoice
 - syncmgr/ISyncMgrConflictResolveInfo::GetItemChoice
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
 - ISyncMgrConflictResolveInfo.GetItemChoice
---

# ISyncMgrConflictResolveInfo::GetItemChoice


## -description

Gets the index of an item that the user wants to keep.

## -parameters

### -param iChoice [in]

Type: <b>UINT</b>

The item that the user wants to keep.

### -param piChoiceIndex [out]

Type: <b>UINT*</b>

The index into the conflict's item array. This value is passed to the resolver for subsequent conflicts in the same conflict set if the user chooses to apply the same operation to all selected conflicts of the same type from the same handler.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setitemchoices">ISyncMgrConflictResolveInfo::SetItemChoices</a>