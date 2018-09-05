---
UID: NF:syncmgr.ISyncMgrConflictStore.GetCount
title: ISyncMgrConflictStore::GetCount
author: windows-sdk-content
description: Gets the number of conflicts in the store.
old-location: shell\ISyncMgrConflictStore_GetCount.htm
old-project: shell
ms.assetid: 1a41bc9a-6f5d-47bf-9186-711292d8be07
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],ISyncMgrConflictStore interface, ISyncMgrConflictStore interface [Windows Shell],GetCount method, ISyncMgrConflictStore.GetCount, ISyncMgrConflictStore::GetCount, _shell_ISyncMgrConflictStore_GetCount, shell.ISyncMgrConflictStore_GetCount, syncmgr/ISyncMgrConflictStore::GetCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrConflictStore.GetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictStore::GetCount


## -description


Gets the number of conflicts in the store.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a sync handler ID as a Unicode string.


### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a sync item ID as a Unicode string.


### -param pnConflicts [out]

Type: <b>DWORD*</b>

When this method returns, contains the conflict count.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



