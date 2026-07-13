---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0005
title: SYNC_RESOLVE_ACTION (winsync.h)
description: Represents actions that are taken to resolve a specific concurrency conflict.
helpviewer_keywords: ["SRA_ACCEPT_DESTINATION_PROVIDER","SRA_ACCEPT_SOURCE_PROVIDER","SRA_DEFER","SRA_LAST","SRA_MERGE","SRA_TRANSFER_AND_DEFER","SYNC_RESOLVE_ACTION","SYNC_RESOLVE_ACTION enumeration [Windows Sync]","winsync.sync_resolve_action","winsync/SRA_ACCEPT_DESTINATION_PROVIDER","winsync/SRA_ACCEPT_SOURCE_PROVIDER","winsync/SRA_DEFER","winsync/SRA_LAST","winsync/SRA_MERGE","winsync/SRA_TRANSFER_AND_DEFER","winsync/SYNC_RESOLVE_ACTION"]
old-location: winsync\sync_resolve_action.htm
tech.root: winsync
ms.assetid: 6549eee1-6bf4-46b0-97d1-bb2c0f1b59a4
ms.date: 12/05/2018
ms.keywords: SRA_ACCEPT_DESTINATION_PROVIDER, SRA_ACCEPT_SOURCE_PROVIDER, SRA_DEFER, SRA_LAST, SRA_MERGE, SRA_TRANSFER_AND_DEFER, SYNC_RESOLVE_ACTION, SYNC_RESOLVE_ACTION enumeration [Windows Sync], winsync.sync_resolve_action, winsync/SRA_ACCEPT_DESTINATION_PROVIDER, winsync/SRA_ACCEPT_SOURCE_PROVIDER, winsync/SRA_DEFER, winsync/SRA_LAST, winsync/SRA_MERGE, winsync/SRA_TRANSFER_AND_DEFER, winsync/SYNC_RESOLVE_ACTION
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SYNC_RESOLVE_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0005
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0005
 - SYNC_RESOLVE_ACTION
 - winsync/SYNC_RESOLVE_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - SYNC_RESOLVE_ACTION
---

# SYNC_RESOLVE_ACTION enumeration


## -description

Represents actions that are taken to resolve a specific concurrency conflict.

## -enum-fields

### -field SRA_DEFER:0

Ignore the conflict and do not apply the change. The change applier does not pass the conflict data to the destination provider.

### -field SRA_ACCEPT_DESTINATION_PROVIDER

The change made on the destination replica wins. Only version information for the item is updated in the metadata on the destination replica. No item data changes are made.

### -field SRA_ACCEPT_SOURCE_PROVIDER

The change made on the source replica wins. The change is applied to the destination replica exactly like any non-conflicting change.

### -field SRA_MERGE

Merge the data from the source item into the destination item. The destination provider combines the source item data and the destination item data, and applies the result to the destination replica.

### -field SRA_TRANSFER_AND_DEFER

Log the conflict and do not apply the change.

### -field SRA_LAST

A placeholder for the last element in the enumeration. Do not use this value.

## -remarks

The members of <b>SYNC_RESOLVE_ACTION</b> specify the action that the change applier uses to resolve a concurrency conflict. Concurrency conflicts occur when the same item or change unit is changed on two different replicas that are later synchronized.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getresolveactionforchange">IChangeConflict::GetResolveActionForChange</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchange">IChangeConflict::SetResolveActionForChange</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
