---
UID: NS:clusapi.CLUS_PARTITION_INFO_EX
title: CLUS_PARTITION_INFO_EX (clusapi.h)
author: windows-sdk-content
description: Describes a storage class resource volume and file system.
old-location: mscs\clus_partition_info_ex.htm
tech.root: MsCS
ms.assetid: d061bcb5-7c4c-4d07-9cdf-fa9f7ac34b3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUS_PARTITION_INFO_EX, CLUSPROP_PIFLAG_DEFAULT_QUORUM, CLUSPROP_PIFLAG_REMOVABLE, CLUSPROP_PIFLAG_STICKY, CLUSPROP_PIFLAG_USABLE, CLUS_PARTITION_INFO_EX, CLUS_PARTITION_INFO_EX structure [Failover Cluster], FS_CASE_IS_PRESERVED, FS_CASE_SENSITIVE, FS_PERSISTENT_ACLS, FS_UNICODE_STORED_ON_DISK, PCLUS_PARTITION_INFO_EX, PCLUS_PARTITION_INFO_EX structure pointer [Failover Cluster], clusapi/CLUS_PARTITION_INFO_EX, clusapi/PCLUS_PARTITION_INFO_EX, mscs.clus_partition_info_ex"
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - CLUS_PARTITION_INFO_EX
product: Windows
targetos: Windows
req.typenames: CLUS_PARTITION_INFO_EX, *PCLUS_PARTITION_INFO_EX
req.redist: 
ms.custom: 19H1
---

# CLUS_PARTITION_INFO_EX structure


## -description


Describes a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">storage class resource</a> volume and file 
    system. It is used as the data member of a 
    <a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a> structure and as the 
    return value of some <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> operations.


## -struct-fields




### -field dwFlags

Flags that describes the storage class resource, enumerated by the 
       <a href="https://msdn.microsoft.com/54597c05-57af-49ad-96e0-171f09c45a65">CLUSPROP_PIFLAGS</a> enumeration.



#### CLUSPROP_PIFLAG_STICKY (1)

The drive letter is sticky.



#### CLUSPROP_PIFLAG_REMOVABLE (2)

The storage class resource is removable.



#### CLUSPROP_PIFLAG_USABLE (4)

The storage class resource is formatted with a file system that is usable by the 
         <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>.



#### CLUSPROP_PIFLAG_DEFAULT_QUORUM (8)

The partition should be used to store quorum files if no partition is specified in the 
         <a href="https://msdn.microsoft.com/1a00c09e-4470-4c02-807d-c559fd992066">SetClusterQuorumResource</a> function. For 
         <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources, the smallest NTFS partition 
         larger than 50MB automatically receives this flag.


### -field szDeviceName

Device name for the storage class resource, such as "C:". No backslashes are included.


### -field szVolumeLabel

Volume label for the storage class resource.


### -field dwSerialNumber

Serial number of the storage class resource volume.


### -field rgdwMaximumComponentLength

Maximum length, in characters, of a file name component supported by the specified file system. A file name 
       component is that portion of a file name between backslashes.


### -field dwFileSystemFlags

Flags that describes the file system. One or more of the following flags are valid.



#### FS_CASE_SENSITIVE (1)

The file system supports case-sensitive file names.



#### FS_CASE_IS_PRESERVED (2)

The file system preserves the case of file names when it places a name on the storage class 
        resource.



#### FS_UNICODE_STORED_ON_DISK (4)

The file system supports Unicode in file names as they appear on storage class resource.



#### FS_PERSISTENT_ACLS (8)

The file system preserves and enforces access control lists (ACLs).


### -field szFileSystem

Name of the file system, such as "FAT" or "NTFS".


### -field TotalSizeInBytes

Specifies the total size, in bytes, of the volume. This value may not be properly aligned and should be accessed using 
       <b>UNALIGNED</b> pointers.


### -field FreeSizeInBytes

Specifies the size, in bytes, of the unallocated space on the volume. This value may not be properly aligned and should be accessed using 
       <b>UNALIGNED</b> pointers.


### -field DeviceNumber

The device number


### -field PartitionNumber

The partition number.


### -field VolumeGuid

The globally unique identifier associated with the volume.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

