---
UID: NS:clusapi._SR_RESOURCE_TYPE_ELIGIBLE_SOURCE_DATADISKS
title: SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS (clusapi.h)
description: Describes a set of retrieved data disks that can be used as source sites for replication.
helpviewer_keywords: ["*PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS","PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS","PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS structure pointer [Failover Cluster]","SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS","SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS structure [Failover Cluster]","clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS","clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS","mscs.sr_resource_type_query_eligible_source_datadisks"]
old-location: mscs\sr_resource_type_query_eligible_source_datadisks.htm
tech.root: MsCS
ms.assetid: DA64413A-0FCB-4D25-A6D0-58C1E978455E
ms.date: 12/05/2018
ms.keywords: '*PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS structure pointer [Failover Cluster], SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS, SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS structure [Failover Cluster], clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS, clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS, mscs.sr_resource_type_query_eligible_source_datadisks'
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
targetos: Windows
req.typenames: SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS, *PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_RESOURCE_TYPE_ELIGIBLE_SOURCE_DATADISKS
 - clusapi/_SR_RESOURCE_TYPE_ELIGIBLE_SOURCE_DATADISKS
 - PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS
 - clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS
 - SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS
 - clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS
---

# SR_RESOURCE_TYPE_QUERY_ELIGIBLE_SOURCE_DATADISKS structure


## -description

Describes a set of retrieved data disks that can be used as source sites for replication.

## -struct-fields

### -field DataDiskGuid

The cluster resource identifier of the data disk.

### -field IncludeAvailableStoargeDisks

<b>true</b> if the result set includes disks in the available storage group.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>