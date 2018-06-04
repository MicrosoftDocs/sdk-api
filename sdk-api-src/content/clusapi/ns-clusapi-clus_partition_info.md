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

# CLUS_PARTITION_INFO structure


## -description


Contains data describing a 
    <a href="s_gly.htm">storage class resource</a> volume and file 
    system. It is used as the data member of a 
    <a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a> structure and as the 
    return value of some <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> operations.


## -struct-fields




### -field dwFlags

Flags that describes the storage class resource, enumerated by the 
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


### -field szDeviceName

Device name for the storage class resource, such as "C:". No backslash is included.


### -field szVolumeLabel

Volume label for the storage class resource.


### -field dwSerialNumber

Serial number of the storage class resource volume.


### -field rgdwMaximumComponentLength

Value of the maximum length, in characters, of a file name component supported by the specified file 
      system. A file name component is the portion of a file name between backslashes.


### -field dwFileSystemFlags

Value that describes the file system. One or more of the following flags are valid.



#### FS_CASE_IS_PRESERVED (0x00000002)

The file system preserves the case of file names when it places a name on the storage class 
        resource.



#### FS_CASE_SENSITIVE (0x00000001)

The file system supports case-sensitive file names.



#### FS_UNICODE_STORED_ON_DISK (0x00000004)

The file system supports Unicode in file names as they appear on storage class resource.



#### FS_PERSISTENT_ACLS (0x00000008)

The file system preserves and enforces access control lists (ACLs).


### -field szFileSystem

Name of the file system, such as "FAT" or "NTFS".


## -remarks



A <b>CLUS_PARTITION_INFO</b> structure can be returned by 
    <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="https://msdn.microsoft.com/e80dfab7-448a-4d68-aae8-c6b42c5dc6f9">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a> 
     and can be returned by 
     <a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="https://msdn.microsoft.com/2df1eeb4-ecad-4065-866c-545476a43d9b">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>.


#### Examples

See 
     <a href="https://msdn.microsoft.com/003bc879-d526-4f7d-8f58-a9002f78819d">Creating Physical Disk Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e80dfab7-448a-4d68-aae8-c6b42c5dc6f9">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a>



<a href="https://msdn.microsoft.com/2df1eeb4-ecad-4065-866c-545476a43d9b">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>



<a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a>
 

 

