---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.SetItemChoices
title: ISyncMgrConflictResolveInfo::SetItemChoices (syncmgr.h)
description: Sets the array of indexes that represents which items the user wants to keep. This method is used when the user chooses to apply the same operation to all selected conflicts of the same type from the same handler.
helpviewer_keywords: ["ISyncMgrConflictResolveInfo interface [Windows Shell]","SetItemChoices method","ISyncMgrConflictResolveInfo.SetItemChoices","ISyncMgrConflictResolveInfo::SetItemChoices","SetItemChoices","SetItemChoices method [Windows Shell]","SetItemChoices method [Windows Shell]","ISyncMgrConflictResolveInfo interface","_shell_ISyncMgrConflictResolveInfo_SetItemChoices","shell.ISyncMgrConflictResolveInfo_SetItemChoices","syncmgr/ISyncMgrConflictResolveInfo::SetItemChoices"]
old-location: shell\ISyncMgrConflictResolveInfo_SetItemChoices.htm
tech.root: shell
ms.assetid: e4485f49-9bcb-47a8-8559-da2217ee1eab
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictResolveInfo interface [Windows Shell],SetItemChoices method, ISyncMgrConflictResolveInfo.SetItemChoices, ISyncMgrConflictResolveInfo::SetItemChoices, SetItemChoices, SetItemChoices method [Windows Shell], SetItemChoices method [Windows Shell],ISyncMgrConflictResolveInfo interface, _shell_ISyncMgrConflictResolveInfo_SetItemChoices, shell.ISyncMgrConflictResolveInfo_SetItemChoices, syncmgr/ISyncMgrConflictResolveInfo::SetItemChoices
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
 - ISyncMgrConflictResolveInfo::SetItemChoices
 - syncmgr/ISyncMgrConflictResolveInfo::SetItemChoices
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
 - ISyncMgrConflictResolveInfo.SetItemChoices
---

# ISyncMgrConflictResolveInfo::SetItemChoices


## -description

Sets the array of indexes that represents which items the user wants to keep. This method is used when the user chooses to apply the same operation to all selected conflicts of the same type from the same handler.

## -parameters

### -param prgiConflictItemIndexes [in]

Type: <b>UINT*</b>

The array of indexes of items that the user wants to keep.

### -param cChoices [in]

Type: <b>UINT</b>

The number of item choices in <i>prgiConflictItemIndexes</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo">ISyncMgrConflictResolveInfo</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoice">ISyncMgrConflictResolveInfo::GetItemChoice</a>