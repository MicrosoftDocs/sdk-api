---
UID: NF:syncmgr.ISyncMgrConflictStore.RemoveConflicts
title: ISyncMgrConflictStore::RemoveConflicts (syncmgr.h)

description: Deletes a set of conflicts, specified by conflict ID, from the store.
old-location: shell\ISyncMgrConflictStore_RemoveConflicts.htm
tech.root: shell
ms.assetid: d6fbb322-7bb0-4ad0-bf01-2fe407689fe5

ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictStore interface [Windows Shell],RemoveConflicts method, ISyncMgrConflictStore.RemoveConflicts, ISyncMgrConflictStore::RemoveConflicts, RemoveConflicts, RemoveConflicts method [Windows Shell], RemoveConflicts method [Windows Shell],ISyncMgrConflictStore interface, _shell_ISyncMgrConflictStore_RemoveConflicts, shell.ISyncMgrConflictStore_RemoveConflicts, syncmgr/ISyncMgrConflictStore::RemoveConflicts
ms.topic: method
f1_keywords: 
 - "syncmgr/ISyncMgrConflictStore.RemoveConflicts"
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
 - ISyncMgrConflictStore.RemoveConflicts
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictStore::RemoveConflicts


## -description


Deletes a set of conflicts, specified by conflict ID, from the store.


## -parameters




### -param rgConflictIdInfo [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ns-syncmgr-syncmgr_conflict_id_info">SYNCMGR_CONFLICT_ID_INFO</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ns-syncmgr-syncmgr_conflict_id_info">SYNCMGR_CONFLICT_ID_INFO</a> structure.


### -param cConflicts [in]

Type: <b>DWORD</b>

The conflict set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The conflicts are removed when the user selects the conflicts in the conflicts folder and chooses to delete them.



