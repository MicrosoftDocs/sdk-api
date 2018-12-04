---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0002
title: "__MIDL___MIDL_itf_winsync_0000_0000_0002"
author: windows-sdk-content
description: Represents the options for the concurrency conflict resolution policy to use for the synchronization session.
old-location: winsync\conflict_resolution_policy.htm
tech.root: winsync
ms.assetid: 4c2f7237-32ac-4f2d-bf6a-7959bc5d40d4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CONFLICT_RESOLUTION_POLICY, CONFLICT_RESOLUTION_POLICY enumeration [Windows Sync], CRP_DESTINATION_PROVIDER_WINS, CRP_LAST, CRP_NONE, CRP_SOURCE_PROVIDER_WINS, __MIDL___MIDL_itf_winsync_0000_0000_0002, winsync.conflict_resolution_policy, winsync/CONFLICT_RESOLUTION_POLICY, winsync/CRP_DESTINATION_PROVIDER_WINS, winsync/CRP_LAST, winsync/CRP_NONE, winsync/CRP_SOURCE_PROVIDER_WINS
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
 - CONFLICT_RESOLUTION_POLICY
product: Windows
targetos: Windows
req.typenames: CONFLICT_RESOLUTION_POLICY
req.redist: 
---

# __MIDL___MIDL_itf_winsync_0000_0000_0002 enumeration


## -description


Represents the options for the concurrency conflict resolution policy to use for the synchronization session.


## -enum-fields




### -field CRP_NONE

The change applier notifies the synchronization application of each conflict as it occurs, by using the <a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">ISyncCallback::OnConflict</a> method. The application examines the conflicting items and specifies the conflict resolution action by calling <a href="https://msdn.microsoft.com/f1a26c85-a00d-408e-96ea-5849c6bb99ff">IChangeConflict::SetResolveActionForChange</a> or <a href="https://msdn.microsoft.com/8594a888-21a1-4cfb-964c-9c670e3a7438">IChangeConflict::SetResolveActionForChangeUnit</a>.


### -field CRP_DESTINATION_PROVIDER_WINS

The change made on the destination replica always wins. This supports the case in which the destination replica does not consume changes that are made by remote clients.


### -field CRP_SOURCE_PROVIDER_WINS

The change made on the source replica always wins. This supports a read-only synchronization solution in which the destination replica is not to be trusted.


### -field CRP_LAST

A placeholder for the last element in the enumeration. Do not use this value.


## -remarks



The members of <b>CONFLICT_RESOLUTION_POLICY</b> are used by a synchronization application to specify the policy that the change applier uses to resolve concurrency conflicts that occur during synchronization. Concurrency conflicts occur when the same item or change unit is changed on two different replicas that are later synchronized.




## -see-also




<a href="https://msdn.microsoft.com/528a109a-9c11-4e20-b3d5-9bb7241d02b6">IKnowledgeSyncProvider::ProcessChangeBatch</a>



<a href="https://msdn.microsoft.com/7d34bc48-377c-4249-a26e-0802dee0b53c">IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch</a>



<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

