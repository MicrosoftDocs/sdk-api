---
UID: NS:clusapi.CLUS_PARTITION_INFO_EX2
title: CLUS_PARTITION_INFO_EX2 (clusapi.h)
description: Describes the disk partition information of a storage class resource.
helpviewer_keywords: ["*PCLUS_PARTITION_INFO_EX2","BitLockerDecrypted","BitLockerDecrypting","BitLockerEnabled","BitLockerEncrypted","BitLockerEncrypting","BitLockerFlagsAll","BitLockerPaused","BitLockerStopped","CLUS_PARTITION_INFO_EX2","CLUS_PARTITION_INFO_EX2 structure [Failover Cluster]","PCLUS_PARTITION_INFO_EX2","PCLUS_PARTITION_INFO_EX2 structure pointer [Failover Cluster]","clusapi/CLUS_PARTITION_INFO_EX2","clusapi/PCLUS_PARTITION_INFO_EX2","mscs.clus_partition_info_ex2"]
old-location: mscs\clus_partition_info_ex2.htm
tech.root: MsCS
ms.assetid: 1B6690DB-9D23-4D0C-98B7-3066C5452CD1
ms.date: 12/05/2018
ms.keywords: '*PCLUS_PARTITION_INFO_EX2, BitLockerDecrypted, BitLockerDecrypting, BitLockerEnabled, BitLockerEncrypted, BitLockerEncrypting, BitLockerFlagsAll, BitLockerPaused, BitLockerStopped, CLUS_PARTITION_INFO_EX2, CLUS_PARTITION_INFO_EX2 structure [Failover Cluster], PCLUS_PARTITION_INFO_EX2, PCLUS_PARTITION_INFO_EX2 structure pointer [Failover Cluster], clusapi/CLUS_PARTITION_INFO_EX2, clusapi/PCLUS_PARTITION_INFO_EX2, mscs.clus_partition_info_ex2'
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
req.typenames: CLUS_PARTITION_INFO_EX2, *PCLUS_PARTITION_INFO_EX2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_PARTITION_INFO_EX2
 - clusapi/CLUS_PARTITION_INFO_EX2
 - PCLUS_PARTITION_INFO_EX2
 - clusapi/PCLUS_PARTITION_INFO_EX2
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
 - CLUS_PARTITION_INFO_EX2
---

# CLUS_PARTITION_INFO_EX2 structure


## -description

Describes the disk partition information of a  
    <a href="/previous-versions/windows/desktop/mscs/s-gly">storage class resource</a>. This structure is used as the data member of a 
    <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex2">CLUSPROP_PARTITION_INFO_EX2</a> structure.

## -struct-fields

### -field GptPartitionId

The globally unique identifier (GUID) of the partition.

### -field szPartitionName

The name of the partition.

### -field EncryptionFlags

A flag that indicates whether BitLocker encryption is enabled on the partition.



#### BitLockerEnabled (0x00000001L)



#### BitLockerDecrypted (0x00000004L)



#### BitLockerEncrypted (0x00000008L)



#### BitLockerDecrypting (0x00000010L)



#### BitLockerEncrypting (0x00000020L)



#### BitLockerPaused (0x00000040L)



#### BitLockerStopped (0x00000080L)



#### BitLockerFlagsAll ((BitLockerEnabled | BitLockerDecrypted | BitlockerEncrypted | BitLockerDecrypting | BitlockerEncrypting | BitLockerPaused | BitLockerStopped)

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info-ex2">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>