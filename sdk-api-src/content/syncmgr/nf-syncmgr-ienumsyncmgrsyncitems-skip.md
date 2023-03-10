---
UID: NF:syncmgr.IEnumSyncMgrSyncItems.Skip
title: IEnumSyncMgrSyncItems::Skip (syncmgr.h)
description: Skips forward in the enumeration the specified number of items.
helpviewer_keywords: ["IEnumSyncMgrSyncItems interface [Windows Shell]","Skip method","IEnumSyncMgrSyncItems.Skip","IEnumSyncMgrSyncItems::Skip","Skip","Skip method [Windows Shell]","Skip method [Windows Shell]","IEnumSyncMgrSyncItems interface","_shell_IEnumSyncMgrSyncItems_Skip","shell.IEnumSyncMgrSyncItems_Skip","syncmgr/IEnumSyncMgrSyncItems::Skip"]
old-location: shell\IEnumSyncMgrSyncItems_Skip.htm
tech.root: shell
ms.assetid: a07038de-84dc-4371-b72f-c835efd73ffc
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrSyncItems interface [Windows Shell],Skip method, IEnumSyncMgrSyncItems.Skip, IEnumSyncMgrSyncItems::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumSyncMgrSyncItems interface, _shell_IEnumSyncMgrSyncItems_Skip, shell.IEnumSyncMgrSyncItems_Skip, syncmgr/IEnumSyncMgrSyncItems::Skip
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
 - IEnumSyncMgrSyncItems::Skip
 - syncmgr/IEnumSyncMgrSyncItems::Skip
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
 - IEnumSyncMgrSyncItems.Skip
---

# IEnumSyncMgrSyncItems::Skip


## -description

Skips forward in the enumeration the specified number of items.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of items to skip.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

