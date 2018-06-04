---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CLUS_PARTITION_INFO_EX2 structure


## -description


Describes the disk partition information of a  
    <a href="s_gly.htm">storage class resource</a>. This structure is used as the data member of a 
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
 

 

