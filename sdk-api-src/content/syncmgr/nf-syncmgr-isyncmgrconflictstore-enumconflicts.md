---
UID: NF:syncmgr.ISyncMgrConflictStore.EnumConflicts
title: ISyncMgrConflictStore::EnumConflicts method
author: windows-driver-content
description: Enumerates conflicts scoped to the provided sync handler and sync item.
old-location: shell\ISyncMgrConflictStore_EnumConflicts.htm
old-project: shell
ms.assetid: b59c679c-7759-4b7a-9a23-f054af99d6a7
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: EnumConflicts method [Windows Shell], EnumConflicts method [Windows Shell], ISyncMgrConflictStore interface, EnumConflicts,ISyncMgrConflictStore.EnumConflicts, ISyncMgrConflictStore, ISyncMgrConflictStore interface [Windows Shell], EnumConflicts method, ISyncMgrConflictStore::EnumConflicts, _shell_ISyncMgrConflictStore_EnumConflicts, shell.ISyncMgrConflictStore_EnumConflicts, syncmgr/ISyncMgrConflictStore::EnumConflicts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrConflictStore.EnumConflicts
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictStore::EnumConflicts method


## -description


Enumerates conflicts scoped to the provided sync handler and sync item.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to the sync handler ID as a Unicode string.


### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to the sync item ID as a Unicode string.


### -param ppEnum [out]

Type: <b><a href="https://msdn.microsoft.com/627f39be-5c9d-49a1-af73-210cdbb7940a">IEnumSyncMgrConflict</a>**</b>

The address of an <a href="https://msdn.microsoft.com/627f39be-5c9d-49a1-af73-210cdbb7940a">IEnumSyncMgrConflict</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the sync handler, sync item, or partner name is <b>NULL</b>, the conflict store ignores that parameter.
           



