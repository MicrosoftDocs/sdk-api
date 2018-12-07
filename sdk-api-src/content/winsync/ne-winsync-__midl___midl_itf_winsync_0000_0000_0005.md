---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0005
title: "__MIDL___MIDL_itf_winsync_0000_0000_0005"
author: windows-sdk-content
description: Represents actions that are taken to resolve a specific concurrency conflict.
old-location: winsync\sync_resolve_action.htm
tech.root: winsync
ms.assetid: 6549eee1-6bf4-46b0-97d1-bb2c0f1b59a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SRA_ACCEPT_DESTINATION_PROVIDER, SRA_ACCEPT_SOURCE_PROVIDER, SRA_DEFER, SRA_LAST, SRA_MERGE, SRA_TRANSFER_AND_DEFER, SYNC_RESOLVE_ACTION, SYNC_RESOLVE_ACTION enumeration [Windows Sync], __MIDL___MIDL_itf_winsync_0000_0000_0005, winsync.sync_resolve_action, winsync/SRA_ACCEPT_DESTINATION_PROVIDER, winsync/SRA_ACCEPT_SOURCE_PROVIDER, winsync/SRA_DEFER, winsync/SRA_LAST, winsync/SRA_MERGE, winsync/SRA_TRANSFER_AND_DEFER, winsync/SYNC_RESOLVE_ACTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - SYNC_RESOLVE_ACTION
product: Windows
targetos: Windows
req.typenames: SYNC_RESOLVE_ACTION
req.redist: 
---

# __MIDL___MIDL_itf_winsync_0000_0000_0005 enumeration


## -description


Represents actions that are taken to resolve a specific concurrency conflict.


## -enum-fields




### -field SRA_DEFER

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




<a href="https://msdn.microsoft.com/b89124fe-200e-4061-974e-2d686de7a932">IChangeConflict::GetResolveActionForChange</a>



<a href="https://msdn.microsoft.com/f1a26c85-a00d-408e-96ea-5849c6bb99ff">IChangeConflict::SetResolveActionForChange</a>



<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

