---
UID: NS:clusapi._SR_RESOURCE_TYPE_ELIGIBLE_TARGET_DATADISKS
title: "_SR_RESOURCE_TYPE_ELIGIBLE_TARGET_DATADISKS"
author: windows-sdk-content
description: Describes a set of retrieved data disks that can be used as target sites for replication.
old-location: mscs\sr_resource_type_query_eligible_target_datadisks.htm
tech.root: mscs
ms.assetid: 3179737F-E4E5-4123-ACFE-235BD0579C52
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS structure pointer [Failover Cluster], SR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS, SR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS structure [Failover Cluster], _SR_RESOURCE_TYPE_ELIGIBLE_TARGET_DATADISKS, clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS, clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS, mscs.sr_resource_type_query_eligible_target_datadisks"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusAPI.h
api_name:
 - SR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS
product: Windows
targetos: Windows
req.typenames: SR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS, *PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_TARGET_DATADISKS
req.redist: 
---

# _SR_RESOURCE_TYPE_ELIGIBLE_TARGET_DATADISKS structure


## -description


Describes a set of retrieved data disks that can be used as target sites for replication.


## -struct-fields




### -field SourceDataDiskGuid

The cluster resource identifier of the data disk.


### -field TargetReplicationGroupGuid

The identifier of the replication group that contains the retrieved data disks.


### -field SkipConnectivityCheck

<b>true</b> if the disks that are connected to the same nodes as the source disk are included in result set.


### -field IncludeOfflineDisks

<b>true</b> if the result set includes all offline disks in the available storage group.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

