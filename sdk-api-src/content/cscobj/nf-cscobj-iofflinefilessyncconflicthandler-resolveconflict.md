---
UID: NF:cscobj.IOfflineFilesSyncConflictHandler.ResolveConflict
title: IOfflineFilesSyncConflictHandler::ResolveConflict (cscobj.h)
description: Provides a resolution decision for a sync conflict.
helpviewer_keywords: ["IOfflineFilesSyncConflictHandler interface [Offline Files]","ResolveConflict method","IOfflineFilesSyncConflictHandler.ResolveConflict","IOfflineFilesSyncConflictHandler::ResolveConflict","OFFLINEFILES_CHANGES_LOCAL_ATTRIBUTES","OFFLINEFILES_CHANGES_LOCAL_SIZE","OFFLINEFILES_CHANGES_LOCAL_TIME","OFFLINEFILES_CHANGES_REMOTE_ATTRIBUTES","OFFLINEFILES_CHANGES_REMOTE_SIZE","OFFLINEFILES_CHANGES_REMOTE_TIME","OFFLINEFILES_SYNC_STATE_LOCAL_KNOWN","OFFLINEFILES_SYNC_STATE_REMOTE_KNOWN","ResolveConflict","ResolveConflict method [Offline Files]","ResolveConflict method [Offline Files]","IOfflineFilesSyncConflictHandler interface","cscobj/IOfflineFilesSyncConflictHandler::ResolveConflict","of.iofflinefilessyncconflicthandler_resolveconflict"]
old-location: of\iofflinefilessyncconflicthandler_resolveconflict.htm
tech.root: of
ms.assetid: eb6fbdcf-1833-4ada-880e-f2dbfce64d99
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncConflictHandler interface [Offline Files],ResolveConflict method, IOfflineFilesSyncConflictHandler.ResolveConflict, IOfflineFilesSyncConflictHandler::ResolveConflict, OFFLINEFILES_CHANGES_LOCAL_ATTRIBUTES, OFFLINEFILES_CHANGES_LOCAL_SIZE, OFFLINEFILES_CHANGES_LOCAL_TIME, OFFLINEFILES_CHANGES_REMOTE_ATTRIBUTES, OFFLINEFILES_CHANGES_REMOTE_SIZE, OFFLINEFILES_CHANGES_REMOTE_TIME, OFFLINEFILES_SYNC_STATE_LOCAL_KNOWN, OFFLINEFILES_SYNC_STATE_REMOTE_KNOWN, ResolveConflict, ResolveConflict method [Offline Files], ResolveConflict method [Offline Files],IOfflineFilesSyncConflictHandler interface, cscobj/IOfflineFilesSyncConflictHandler::ResolveConflict, of.iofflinefilessyncconflicthandler_resolveconflict
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesSyncConflictHandler::ResolveConflict
 - cscobj/IOfflineFilesSyncConflictHandler::ResolveConflict
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSyncConflictHandler.ResolveConflict
---

# IOfflineFilesSyncConflictHandler::ResolveConflict


## -description

Provides a resolution decision for a sync conflict.

## -parameters

### -param pszPath [in]

The fully qualified UNC path of the item in conflict.

### -param fStateKnown [in]

Indicates if the sync state was based on the client state, server state, or both.  This parameter can be one or both of the following flag values.



#### OFFLINEFILES_SYNC_STATE_LOCAL_KNOWN (0x00000001)

The sync state was based on the client state.



#### OFFLINEFILES_SYNC_STATE_REMOTE_KNOWN (0x00000002)

The sync state was based on the server state.

### -param state [in]

A value from the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_sync_state">OFFLINEFILES_SYNC_STATE</a> enumeration indicating the state of the item in conflict.

### -param fChangeDetails [in]

In cases where the <i>state</i> code indicates a change in item state, this value describes the change in further detail.  The value can be either <b>OFFLINEFILES_CHANGES_NONE</b> (0x00000000) or one or more of the following flag values:



#### OFFLINEFILES_CHANGES_LOCAL_SIZE (0x00000001)

Local file size has changed.



#### OFFLINEFILES_CHANGES_LOCAL_ATTRIBUTES (0x00000002)

Local file attributes have changed.



#### OFFLINEFILES_CHANGES_LOCAL_TIME (0x00000004)

Local file change time has changed.



#### OFFLINEFILES_CHANGES_REMOTE_SIZE (0x00000008)

Remote file size has changed.



#### OFFLINEFILES_CHANGES_REMOTE_ATTRIBUTES (0x00000010)

Remote file attributes have changed.



#### OFFLINEFILES_CHANGES_REMOTE_TIME (0x00000020)

Remote file change time has changed.

### -param pConflictResolution [out]

Receives the desired resolution code.  Specify a value from the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_sync_conflict_resolve">OFFLINEFILES_SYNC_CONFLICT_RESOLVE</a> enumeration.

### -param ppszNewName [out]

If the value of the  <i>pConflictResolution</i> parameter is <b>OFFLINEFILES_SYNC_CONFLICT_RESOLVE_KEEPALLCHANGES</b>, the conflict handler must provide a new name for the item.  This new name is used for the new copies created remotely and locally.  Note that this is a file name, not a fully qualified path.

The name string must be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>.

This parameter may be <b>NULL</b> if a new name is not required by the resolution.

The Offline Files conflict handler used by Sync Center creates a name of the following format:

&lt;original name&gt; (&lt;user name&gt; v<i>N</i>).&lt;original ext&gt;

where <i>N</i> is a version number. Therefore, if the original file name is "samples.doc" and the user's name is "Alice", the new file name will be:

"samples (Alice v1).doc"

If a file of that name exists the Offline Files conflict handler increments <i>N</i> until a unique name is found, for example:

<ul>
<li>samples (Alice v2).doc</li>
<li>samples (Alice v3).doc</li>
</ul>
This description is provided only to illustrate how the Offline Files conflict handler in Sync Center creates new file names.  An implementation of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncconflicthandler">IOfflineFilesSyncConflictHandler</a> is free to use any name format that it wishes to define.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncconflicthandler">IOfflineFilesSyncConflictHandler</a>