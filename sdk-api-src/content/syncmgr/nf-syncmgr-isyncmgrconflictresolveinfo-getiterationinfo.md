---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetIterationInfo
title: ISyncMgrConflictResolveInfo::GetIterationInfo (syncmgr.h)
description: Gets information about which conflict in a set of conflicts is being resolved.
helpviewer_keywords: ["GetIterationInfo","GetIterationInfo method [Windows Shell]","GetIterationInfo method [Windows Shell]","ISyncMgrConflictResolveInfo interface","ISyncMgrConflictResolveInfo interface [Windows Shell]","GetIterationInfo method","ISyncMgrConflictResolveInfo.GetIterationInfo","ISyncMgrConflictResolveInfo::GetIterationInfo","_shell_ISyncMgrConflictResolveInfo_GetIterationInfo","shell.ISyncMgrConflictResolveInfo_GetIterationInfo","syncmgr/ISyncMgrConflictResolveInfo::GetIterationInfo"]
old-location: shell\ISyncMgrConflictResolveInfo_GetIterationInfo.htm
tech.root: shell
ms.assetid: ac22d346-3012-41b0-a655-062f501af621
ms.date: 12/05/2018
ms.keywords: GetIterationInfo, GetIterationInfo method [Windows Shell], GetIterationInfo method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetIterationInfo method, ISyncMgrConflictResolveInfo.GetIterationInfo, ISyncMgrConflictResolveInfo::GetIterationInfo, _shell_ISyncMgrConflictResolveInfo_GetIterationInfo, shell.ISyncMgrConflictResolveInfo_GetIterationInfo, syncmgr/ISyncMgrConflictResolveInfo::GetIterationInfo
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
 - ISyncMgrConflictResolveInfo::GetIterationInfo
 - syncmgr/ISyncMgrConflictResolveInfo::GetIterationInfo
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
 - ISyncMgrConflictResolveInfo.GetIterationInfo
---

# ISyncMgrConflictResolveInfo::GetIterationInfo


## -description

Gets information about which conflict in a set of conflicts is being resolved.

## -parameters

### -param pnCurrentConflict [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the index of the conflict in the set that is being resolved.

### -param pcConflicts [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of conflicts that are being resolved.

### -param pcRemainingForApplyToAll [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of the remaining conflicts to which an "apply to all" response would be applied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

