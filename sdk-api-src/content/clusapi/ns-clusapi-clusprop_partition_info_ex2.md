---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO_EX2
title: CLUSPROP_PARTITION_INFO_EX2 (clusapi.h)
description: A value list entry that contains partition information for a storage class resource. This structure is as a input, and a as a return value for the CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2 control code.
helpviewer_keywords: ["*PCLUSPROP_PARTITION_INFO_EX2","CLUSPROP_PARTITION_INFO_EX2","CLUSPROP_PARTITION_INFO_EX2 structure [Failover Cluster]","clusapi/CLUSPROP_PARTITION_INFO_EX2","mscs.clusprop_partition_info_ex2"]
old-location: mscs\clusprop_partition_info_ex2.htm
tech.root: MsCS
ms.assetid: D6D26335-80D0-4949-99B4-FE18DD2FFF3C
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_PARTITION_INFO_EX2, CLUSPROP_PARTITION_INFO_EX2, CLUSPROP_PARTITION_INFO_EX2 structure [Failover Cluster], clusapi/CLUSPROP_PARTITION_INFO_EX2, mscs.clusprop_partition_info_ex2'
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
req.typenames: CLUSPROP_PARTITION_INFO_EX2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_PARTITION_INFO_EX2
 - clusapi/CLUSPROP_PARTITION_INFO_EX2
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
 - CLUSPROP_PARTITION_INFO_EX2
---

# CLUSPROP_PARTITION_INFO_EX2 structure


## -description

A value list entry that contains partition information for a storage class resource. This structure is as a input, and a as a return value for the <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info-ex2">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2</a> control code.

## -struct-fields

### -field CLUSPROP_PARTITION_INFO_EX

A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex">CLUSPROP_PARTITION_INFO_EX</a> structure that describes the format, 
     type, and length of the partition information.

### -field CLUS_PARTITION_INFO_EX2

A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_partition_info_ex2">CLUS_PARTITION_INFO_EX2</a> structure that contains the values of the partition information.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>