---
UID: NF:syncmgr.ISyncMgrConflictStore.RemoveConflicts
title: ISyncMgrConflictStore::RemoveConflicts
author: windows-sdk-content
description: Deletes a set of conflicts, specified by conflict ID, from the store.
old-location: shell\ISyncMgrConflictStore_RemoveConflicts.htm
old-project: shell
ms.assetid: d6fbb322-7bb0-4ad0-bf01-2fe407689fe5
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ISyncMgrConflictStore interface [Windows Shell],RemoveConflicts method, ISyncMgrConflictStore.RemoveConflicts, ISyncMgrConflictStore::RemoveConflicts, RemoveConflicts, RemoveConflicts method [Windows Shell], RemoveConflicts method [Windows Shell],ISyncMgrConflictStore interface, _shell_ISyncMgrConflictStore_RemoveConflicts, shell.ISyncMgrConflictStore_RemoveConflicts, syncmgr/ISyncMgrConflictStore::RemoveConflicts
ms.prod: windows
ms.technology: windows-sdk
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
 - ISyncMgrConflictStore.RemoveConflicts
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictStore::RemoveConflicts


## -description


Deletes a set of conflicts, specified by conflict ID, from the store.


## -parameters




### -param rgConflictIdInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/9a54ef7e-0b22-436e-891b-80610ddaef00">SYNCMGR_CONFLICT_ID_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9a54ef7e-0b22-436e-891b-80610ddaef00">SYNCMGR_CONFLICT_ID_INFO</a> structure.


### -param cConflicts [in]

Type: <b>DWORD</b>

The conflict set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The conflicts are removed when the user selects the conflicts in the conflicts folder and chooses to delete them.



