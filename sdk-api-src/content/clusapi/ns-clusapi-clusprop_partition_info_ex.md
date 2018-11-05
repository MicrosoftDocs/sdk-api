---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO_EX
title: CLUSPROP_PARTITION_INFO_EX
author: windows-sdk-content
description: The CLUSPROP_PARTITION_INFO_EX structure contains information relevant to storage class resources.
old-location: mscs\clusprop_partition_info_ex.htm
tech.root: mscs
ms.assetid: b1343a04-b8bd-469a-a620-985eeb89401c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PCLUSPROP_PARTITION_INFO_EX, CLUSPROP_PARTITION_INFO_EX, CLUSPROP_PARTITION_INFO_EX structure [Failover Cluster], CLUSPROP_PIFLAG_DEFAULT_QUORUM, CLUSPROP_PIFLAG_REMOVABLE, CLUSPROP_PIFLAG_STICKY, CLUSPROP_PIFLAG_USABLE, FS_CASE_IS_PRESERVED, FS_CASE_SENSITIVE, FS_PERSISTENT_ACLS, FS_UNICODE_STORED_ON_DISK, PCLUSPROP_PARTITION_INFO_EX, PCLUSPROP_PARTITION_INFO_EX structure pointer [Failover Cluster], clusapi/CLUSPROP_PARTITION_INFO_EX, clusapi/PCLUSPROP_PARTITION_INFO_EX, mscs.clusprop_partition_info_ex"
ms.prod: windows
ms.technology: windows-sdk
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
 - CLUSPROP_PARTITION_INFO_EX
product: Windows
targetos: Windows
req.typenames: CLUSPROP_PARTITION_INFO_EX
req.redist: 
---

# CLUSPROP_PARTITION_INFO_EX structure


## -description


Specifies a collection of information about a physical disk resource, such as its device name and volume label. 
    The <b>CLUSPROP_PARTITION_INFO_EX</b> 
    structure contains information relevant to 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">storage class resources</a>. It is 
    used as an entry in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
     structure.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> and 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> members are listed 
    explicitly.


## -struct-fields




### -field CLUSPROP_VALUE

 


### -field CLUS_PARTITION_INFO_EX

 




#### - DeviceNumber

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that contains an unsigned 32-bit integer indicating the unique device number.


#### - FreeSizeInBytes

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that identifies the amount of unallocated space, in bytes, of the specified storage class 
       resource.


#### - PartitionNumber

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that identifies the partition number of the specified storage class resource.


#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_PARTITION_INFO_EX</b> (0x000d0001).


#### - TotalSizeInBytes

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that identifies the total size, in bytes, of the specified storage class resource.


#### - VolumeGuid

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that takes a 128-bit value that contains the unique identifier associated with that volume.


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the 
       <b>CLUSPROP_PARTITION_INFO_EX</b> structure.


#### - dwFileSystemFlags

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that describes the file system. One or more of the following flags are valid.



#### FS_CASE_SENSITIVE (1)

The file system supports case-sensitive file names.



#### FS_CASE_IS_PRESERVED (2)

The file system preserves the case of file names when it places a name on the storage class 
         resource.



#### FS_UNICODE_STORED_ON_DISK (4)

The file system supports Unicode in file names as they appear on storage class resource.



#### FS_PERSISTENT_ACLS (8)

The file system preserves and enforces access control lists (ACLs).


#### - dwFlags

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
      structure that describes the storage class resource, enumerated by the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb309114(v=VS.85).aspx">CLUSPROP_PIFLAGS</a> enumeration.



#### CLUSPROP_PIFLAG_STICKY (1)

The drive letter is sticky.



#### CLUSPROP_PIFLAG_REMOVABLE (2)

The storage class resource is removable.



#### CLUSPROP_PIFLAG_USABLE (4)

The storage class resource is formatted with a file system that is usable by the 
        <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a>.



#### CLUSPROP_PIFLAG_DEFAULT_QUORUM (8)

The partition should be used to store quorum files if no partition is specified in the 
        <a href="https://msdn.microsoft.com/1a00c09e-4470-4c02-807d-c559fd992066">SetClusterQuorumResource</a> function. For 
        <a href="https://msdn.microsoft.com/en-us/library/Aa371789(v=VS.85).aspx">Physical Disk</a> resources, the smallest NTFS partition 
        larger than 50MB automatically receives this flag.


#### - dwSerialNumber

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that describes the serial number of the storage class resource volume.


#### - rgdwMaximumComponentLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that describes the maximum length, in characters, of a file name component supported by the specified 
       file system. A file name component is that portion of a file name between backslashes.


#### - szDeviceName

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that describes the device name for the storage class resource, such as C:. No backslashes are 
       included.


#### - szFileSystem

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that describes the name of the file system, such as "FAT" or 
       "NTFS".


#### - szVolumeLabel

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a> 
       structure that describes the volume label for the storage class resource.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368381(v=VS.85).aspx">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309114(v=VS.85).aspx">CLUSPROP_PIFLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309204(v=VS.85).aspx">CLUS_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>
 

 

