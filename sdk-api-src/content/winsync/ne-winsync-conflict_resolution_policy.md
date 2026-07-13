---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0002
title: CONFLICT_RESOLUTION_POLICY (winsync.h)
description: Represents the options for the concurrency conflict resolution policy to use for the synchronization session.
helpviewer_keywords: ["CONFLICT_RESOLUTION_POLICY","CONFLICT_RESOLUTION_POLICY enumeration [Windows Sync]","CRP_DESTINATION_PROVIDER_WINS","CRP_LAST","CRP_NONE","CRP_SOURCE_PROVIDER_WINS","winsync.conflict_resolution_policy","winsync/CONFLICT_RESOLUTION_POLICY","winsync/CRP_DESTINATION_PROVIDER_WINS","winsync/CRP_LAST","winsync/CRP_NONE","winsync/CRP_SOURCE_PROVIDER_WINS"]
old-location: winsync\conflict_resolution_policy.htm
tech.root: winsync
ms.assetid: 4c2f7237-32ac-4f2d-bf6a-7959bc5d40d4
ms.date: 12/05/2018
ms.keywords: CONFLICT_RESOLUTION_POLICY, CONFLICT_RESOLUTION_POLICY enumeration [Windows Sync], CRP_DESTINATION_PROVIDER_WINS, CRP_LAST, CRP_NONE, CRP_SOURCE_PROVIDER_WINS, winsync.conflict_resolution_policy, winsync/CONFLICT_RESOLUTION_POLICY, winsync/CRP_DESTINATION_PROVIDER_WINS, winsync/CRP_LAST, winsync/CRP_NONE, winsync/CRP_SOURCE_PROVIDER_WINS
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
req.typenames: CONFLICT_RESOLUTION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0002
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0002
 - CONFLICT_RESOLUTION_POLICY
 - winsync/CONFLICT_RESOLUTION_POLICY
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
 - CONFLICT_RESOLUTION_POLICY
---

# CONFLICT_RESOLUTION_POLICY enumeration


## -description

Represents the options for the concurrency conflict resolution policy to use for the synchronization session.

## -enum-fields

### -field CRP_NONE:0

The change applier notifies the synchronization application of each conflict as it occurs, by using the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onconflict">ISyncCallback::OnConflict</a> method. The application examines the conflicting items and specifies the conflict resolution action by calling <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchange">IChangeConflict::SetResolveActionForChange</a> or <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchangeunit">IChangeConflict::SetResolveActionForChangeUnit</a>.

### -field CRP_DESTINATION_PROVIDER_WINS

The change made on the destination replica always wins. This supports the case in which the destination replica does not consume changes that are made by remote clients.

### -field CRP_SOURCE_PROVIDER_WINS

The change made on the source replica always wins. This supports a read-only synchronization solution in which the destination replica is not to be trusted.

### -field CRP_LAST

A placeholder for the last element in the enumeration. Do not use this value.

## -remarks

The members of <b>CONFLICT_RESOLUTION_POLICY</b> are used by a synchronization application to specify the policy that the change applier uses to resolve concurrency conflicts that occur during synchronization. Concurrency conflicts occur when the same item or change unit is changed on two different replicas that are later synchronized.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processchangebatch">IKnowledgeSyncProvider::ProcessChangeBatch</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processfullenumerationchangebatch">IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
