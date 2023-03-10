---
UID: NE:cscobj.tagOFFLINEFILES_SYNC_CONFLICT_RESOLVE
title: OFFLINEFILES_SYNC_CONFLICT_RESOLVE (cscobj.h)
description: Identifies the conflict resolution code returned by the IOfflineFilesSyncConflictHandler::ResolveConflict method.
helpviewer_keywords: ["OFFLINEFILES_SYNC_CONFLICT_ABORT","OFFLINEFILES_SYNC_CONFLICT_RESOLVE","OFFLINEFILES_SYNC_CONFLICT_RESOLVE enumeration [Offline Files]","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLATEST","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLOCAL","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPREMOTE","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_LOG","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_NONE","OFFLINEFILES_SYNC_CONFLICT_RESOLVE_SKIP","cscobj/OFFLINEFILES_SYNC_CONFLICT_ABORT","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLATEST","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLOCAL","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPREMOTE","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_LOG","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_NONE","cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_SKIP","of.offlinefiles_sync_conflict_resolve"]
old-location: of\offlinefiles_sync_conflict_resolve.htm
tech.root: of
ms.assetid: 2082b476-cb98-4845-885a-56731f8a4762
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_SYNC_CONFLICT_ABORT, OFFLINEFILES_SYNC_CONFLICT_RESOLVE, OFFLINEFILES_SYNC_CONFLICT_RESOLVE enumeration [Offline Files], OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES, OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLATEST, OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLOCAL, OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPREMOTE, OFFLINEFILES_SYNC_CONFLICT_RESOLVE_LOG, OFFLINEFILES_SYNC_CONFLICT_RESOLVE_NONE, OFFLINEFILES_SYNC_CONFLICT_RESOLVE_SKIP, cscobj/OFFLINEFILES_SYNC_CONFLICT_ABORT, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLATEST, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLOCAL, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPREMOTE, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_LOG, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_NONE, cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE_SKIP, of.offlinefiles_sync_conflict_resolve
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFFLINEFILES_SYNC_CONFLICT_RESOLVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_SYNC_CONFLICT_RESOLVE
 - cscobj/tagOFFLINEFILES_SYNC_CONFLICT_RESOLVE
 - OFFLINEFILES_SYNC_CONFLICT_RESOLVE
 - cscobj/OFFLINEFILES_SYNC_CONFLICT_RESOLVE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_SYNC_CONFLICT_RESOLVE
---

# OFFLINEFILES_SYNC_CONFLICT_RESOLVE enumeration


## -description

Identifies the conflict resolution code returned by the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncconflicthandler-resolveconflict">IOfflineFilesSyncConflictHandler::ResolveConflict</a> method.

## -enum-fields

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_NONE:0

No resolution.  The conflict is unresolved.  This allows the conflict to be processed by other handlers in the system.

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLOCAL

Keep the local state.  This overwrites the remote copy with the local copy's contents.  If the local copy was deleted, this deletes the remote copy on the server.

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPREMOTE

Keep the remote state.  This overwrites the local copy with the remote copy's contents.  If the remote copy was deleted, this deletes the local copy in the Offline Files cache.

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES

Keeps both copies.  Note that this resolution is valid only for sync conflict states where both the server and client copies exist and where at least one of the items is a file.  The <b>OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES</b> resolution is not available when one of the items has been deleted or both items are directories.

The list of applicable <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_sync_state">OFFLINEFILES_SYNC_STATE</a> values is as follows:

<b>OFFLINEFILES_SYNC_STATE_DirChangedOnClient_FileChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_DirChangedOnClient_FileOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_FileChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_DirCreatedOnClient_FileOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_DirOnClient_FileChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_DirOnClient_FileOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileChangedOnClient_ChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileChangedOnClient_DirChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileChangedOnClient_DirOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_DirChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_DirOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_FileChangedOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileCreatedOnClient_FileOnServer</b>
<b>OFFLINEFILES_SYNC_STATE_FileOnClient_DirOnServer</b>

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLATEST

Retains the state of the latest operation as determined by last-change times of the items in conflict.  If the local item was deleted, the time of deletion is used for comparison.

The case where the remote copy was deleted after the client copy was changed is a special case that produces an unexpected result.  The logical expectation is that the later operation (the remote deletion) propagates to the client and deletes the client copy from the cache.  However, the result is that the client copy is restored to the server, reversing the deletion.  This is because Offline Files is a client feature and therefore is unable to know when a remote copy of a cached item was deleted.  If the local copy is modified offline, the last-change time of that local copy will be later than the last-change time for the remote copy recorded when the item was last in sync.  Therefore, an <b>OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPLATEST</b> resolution finds the last-change time on the client copy to be later than the last-change time last known for the server copy.  This causes the local copy to be restored to the server.

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_LOG

Write an entry to the sync conflict log and perform no further attempts at resolving the conflict.  The interactive user will resolve the conflict through Sync Center at a later time.

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_SKIP

Do not resolve the conflict.  Do not record an entry in the sync conflict log.

### -field OFFLINEFILES_SYNC_CONFLICT_ABORT

Cancel the synchronization operation.

### -field OFFLINEFILES_SYNC_CONFLICT_RESOLVE_NUMCODES

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncconflicthandler-resolveconflict">IOfflineFilesSyncConflictHandler::ResolveConflict</a>



<a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_sync_state">OFFLINEFILES_SYNC_STATE</a>
