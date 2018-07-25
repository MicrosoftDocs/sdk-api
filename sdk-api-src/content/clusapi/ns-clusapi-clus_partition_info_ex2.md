---
UID: NS:clusapi.CLUS_PARTITION_INFO_EX2
title: CLUS_PARTITION_INFO_EX2
author: windows-sdk-content
description: Describes the disk partition information of a storage class resource.
old-location: mscs\clus_partition_info_ex2.htm
old-project: mscs
ms.assetid: 1B6690DB-9D23-4D0C-98B7-3066C5452CD1
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PCLUS_PARTITION_INFO_EX2, BitLockerDecrypted, BitLockerDecrypting, BitLockerEnabled, BitLockerEncrypted, BitLockerEncrypting, BitLockerFlagsAll, BitLockerPaused, BitLockerStopped, CLUS_PARTITION_INFO_EX2, CLUS_PARTITION_INFO_EX2 structure [Failover Cluster], PCLUS_PARTITION_INFO_EX2, PCLUS_PARTITION_INFO_EX2 structure pointer [Failover Cluster], clusapi/CLUS_PARTITION_INFO_EX2, clusapi/PCLUS_PARTITION_INFO_EX2, mscs.clus_partition_info_ex2"
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
tech.root: 
req.typenames: CLUS_PARTITION_INFO_EX2, *PCLUS_PARTITION_INFO_EX2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_PARTITION_INFO_EX2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUS_PARTITION_INFO_EX2 structure


## -description


Describes the disk partition information of a  
    <a href="https://msdn.microsoft.com/library/ms682866(v=VS.85).aspx">storage class resource</a>. This structure is used as the data member of a 
    <a href="https://msdn.microsoft.com/D6D26335-80D0-4949-99B4-FE18DD2FFF3C">CLUSPROP_PARTITION_INFO_EX2</a> structure.


## -struct-fields




### -field GptPartitionId

The globally unique identifier (GUID) of the partition.


### -field szPartitionName

The name of the partition.


### -field EncryptionFlags

A flag that indicates whether BitLocker encryption is enabled on the partion.



#### BitLockerEnabled (0x00000001L)



#### BitLockerDecrypted (0x00000004L)



#### BitLockerEncrypted (0x00000008L)



#### BitLockerDecrypting (0x00000010L)



#### BitLockerEncrypting (0x00000020L)



#### BitLockerPaused (0x00000040L)



#### BitLockerStopped (0x00000080L)



#### BitLockerFlagsAll ((BitLockerEnabled | BitLockerDecrypted | BitlockerEncrypted | BitLockerDecrypting | BitlockerEncrypting | BitLockerPaused | BitLockerStopped)


## -see-also




<a href="https://msdn.microsoft.com/FA742D78-D89D-472D-B5C9-6C8D95883CD1">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

