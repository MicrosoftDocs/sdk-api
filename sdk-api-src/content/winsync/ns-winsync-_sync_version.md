---
UID: NS:winsync._SYNC_VERSION
title: "_SYNC_VERSION"
author: windows-sdk-content
description: Represents a version for an item or a change unit.
old-location: winsync\sync_version.htm
tech.root: winsync
ms.assetid: 6a493a58-3dab-4032-90de-be9f903ae489
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SYNC_VERSION, SYNC_VERSION structure [Windows Sync], _SYNC_VERSION, winsync.sync_version, winsync/SYNC_VERSION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - SYNC_VERSION
product: Windows
targetos: Windows
req.typenames: SYNC_VERSION
req.redist: 
---

# _SYNC_VERSION structure


## -description


Represents a version for an item or a change unit.


## -struct-fields




### -field dwLastUpdatingReplicaKey

The replica key that is associated with the version.


### -field ullTickCount

The tick count that is associated with the version.


## -remarks



A change that is made directly to a replica, such as a change that is made by a local application, will not have a version for the change in the synchronization metadata. A version that is created for such a change must contain the following elements:

<ul>
<li>The replica key of the local replica. This will typically be zero.</li>
<li>The current value of the tick count of the local replica.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/40aa741a-b536-4a8b-9f97-b7b599e49aef">IEnumClockVector::Next Method</a>



<a href="https://msdn.microsoft.com/63ea1fdc-5200-40d4-a42a-dcda0318f602">IForgottenKnowledge::ForgetToVersion Method</a>



<a href="https://msdn.microsoft.com/6b6def94-8c48-41f6-8869-e28d0db0d500">ISyncChange::GetChangeVersion Method</a>



<a href="https://msdn.microsoft.com/2c795cbe-b587-42ef-9200-b7d0d972e7c7">ISyncChange::GetCreationVersion Method</a>



<a href="https://msdn.microsoft.com/cb5b5a35-70d9-413d-8bf6-7003fe7681c8">ISyncChangeBatchBase::AddItemMetadataToGroup Method</a>



<a href="https://msdn.microsoft.com/218e0f9d-9471-4b21-a424-b1298da2fb23">ISyncChangeBuilder::AddChangeUnitMetadata Method</a>



<a href="https://msdn.microsoft.com/b40ec132-0459-4ddf-9156-bce2a1dfbc4d">ISyncChangeUnit::GetChangeUnitVersion Method</a>



<a href="https://msdn.microsoft.com/4c304d76-f27a-4382-99ad-1d158da93de6">ISyncKnowledge::ContainsChange Method</a>



<a href="https://msdn.microsoft.com/67fc3b59-ad82-47a4-9fc6-2d980b9e26fe">ISyncKnowledge::ContainsChangeUnit Method</a>



<a href="https://msdn.microsoft.com/f41edaa3-7c4e-4b2c-9897-474b3e7bfb67">ISyncKnowledge::ConvertVersion Method</a>



<a href="https://msdn.microsoft.com/eed33384-f8bd-4a3a-8d04-b59c534f9114">Windows Sync Structures</a>
 

 

