---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO
title: CLUSPROP_PARTITION_INFO
author: windows-sdk-content
description: Contains information relevant to storage class resources.
old-location: mscs\clusprop_partition_info.htm
tech.root: mscs
ms.assetid: cda1e334-dba8-4fe9-b035-4e475245869c
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "*PCLUSPROP_PARTITION_INFO, CLUSPROP_PARTITION_INFO, CLUSPROP_PARTITION_INFO structure [Failover Cluster], CLUSPROP_PIFLAG_DEFAULT_QUORUM, CLUSPROP_PIFLAG_REMOVABLE, CLUSPROP_PIFLAG_STICKY, CLUSPROP_PIFLAG_USABLE, FS_CASE_IS_PRESERVED, FS_CASE_SENSITIVE, FS_PERSISTENT_ACLS, FS_UNICODE_STORED_ON_DISK, PCLUSPROP_PARTITION_INFO, PCLUSPROP_PARTITION_INFO structure pointer [Failover Cluster], _wolf_clusprop_partition_info, clusapi/CLUSPROP_PARTITION_INFO, clusapi/PCLUSPROP_PARTITION_INFO, mscs.clusprop_partition_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - CLUSPROP_PARTITION_INFO
product: Windows
targetos: Windows
req.typenames: CLUSPROP_PARTITION_INFO, *PCLUSPROP_PARTITION_INFO
req.redist: 
---

# CLUSPROP_PARTITION_INFO structure


## -description


Contains 
    information relevant to 
    <a href="s_gly.htm">storage class resources</a>. It is used as an 
    entry in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> and 
    <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> members are listed 
    explicitly.


## -struct-fields




### -field CLUSPROP_VALUE

 


### -field CLUS_PARTITION_INFO

 




#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_PARTITION_INFO</b> (0x00080001).


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
      the count of bytes in the 
      <b>CLUSPROP_PARTITION_INFO</b> structure.


#### - dwFileSystemFlags

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the file system. One or more of the following flags are valid.



#### FS_CASE_IS_PRESERVED (0x00000002)

The file system preserves the case of file names when it places a name on the storage class resource.



#### FS_CASE_SENSITIVE (0x00000001)

The file system supports case-sensitive file names.



#### FS_UNICODE_STORED_ON_DISK (0x00000004)

The file system supports Unicode in file names as they appear on storage class resource.



#### FS_PERSISTENT_ACLS (0x00000008)

The file system preserves and enforces access control lists (ACLs).


#### - dwFlags

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the storage class resource, enumerated by the 
       <a href="https://msdn.microsoft.com/54597c05-57af-49ad-96e0-171f09c45a65">CLUSPROP_PIFLAGS</a> enumeration.



#### CLUSPROP_PIFLAG_STICKY (0x00000001)

The drive letter is sticky.



#### CLUSPROP_PIFLAG_REMOVABLE (0x00000002)

The storage class resource is removable.



#### CLUSPROP_PIFLAG_USABLE (0x00000004)

The storage class resource is formatted with a file system that is usable by the 
         <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>.



#### CLUSPROP_PIFLAG_DEFAULT_QUORUM (0x00000008)

The partition should be used to store quorum files if no partition is specified in the 
         <a href="https://msdn.microsoft.com/1a00c09e-4470-4c02-807d-c559fd992066">SetClusterQuorumResource</a> function. For 
         <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources, the smallest NTFS partition 
         larger than 50MB automatically receives this flag.


#### - dwSerialNumber

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the serial number of the storage class resource volume.


#### - rgdwMaximumComponentLength

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the maximum length, in characters, of a file name component supported by the specified file 
       system. A file name component is that portion of a file name between backslashes.


#### - szDeviceName

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the device name for the storage class resource, such as "C:". No backslashes 
       are included.


#### - szFileSystem

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the name of the file system, such as "FAT" or "NTFS".


#### - szVolumeLabel

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the volume label for the storage class resource.


## -see-also




<a href="https://msdn.microsoft.com/54597c05-57af-49ad-96e0-171f09c45a65">CLUSPROP_PIFLAGS</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

