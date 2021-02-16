---
UID: NS:clusapi.CLUS_PARTITION_INFO
title: CLUS_PARTITION_INFO (clusapi.h)
description: Contains data describing a storage class resource volume and file system. It is used as the data member of a CLUSPROP_PARTITION_INFO structure and as the return value of some control code operations.
helpviewer_keywords: ["*PCLUS_PARTITION_INFO","CLUSPROP_PIFLAG_DEFAULT_QUORUM","CLUSPROP_PIFLAG_REMOVABLE","CLUSPROP_PIFLAG_STICKY","CLUSPROP_PIFLAG_USABLE","CLUS_PARTITION_INFO","CLUS_PARTITION_INFO structure [Failover Cluster]","FS_CASE_IS_PRESERVED","FS_CASE_SENSITIVE","FS_PERSISTENT_ACLS","FS_UNICODE_STORED_ON_DISK","PCLUS_PARTITION_INFO","PCLUS_PARTITION_INFO structure pointer [Failover Cluster]","_wolf_clus_partition_info","clusapi/CLUS_PARTITION_INFO","clusapi/PCLUS_PARTITION_INFO","mscs.clus_partition_info"]
old-location: mscs\clus_partition_info.htm
tech.root: MsCS
ms.assetid: 656b230d-b4ba-45e4-b6b3-8bbe72f9428a
ms.date: 12/05/2018
ms.keywords: '*PCLUS_PARTITION_INFO, CLUSPROP_PIFLAG_DEFAULT_QUORUM, CLUSPROP_PIFLAG_REMOVABLE, CLUSPROP_PIFLAG_STICKY, CLUSPROP_PIFLAG_USABLE, CLUS_PARTITION_INFO, CLUS_PARTITION_INFO structure [Failover Cluster], FS_CASE_IS_PRESERVED, FS_CASE_SENSITIVE, FS_PERSISTENT_ACLS, FS_UNICODE_STORED_ON_DISK, PCLUS_PARTITION_INFO, PCLUS_PARTITION_INFO structure pointer [Failover Cluster], _wolf_clus_partition_info, clusapi/CLUS_PARTITION_INFO, clusapi/PCLUS_PARTITION_INFO, mscs.clus_partition_info'
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
targetos: Windows
req.typenames: CLUS_PARTITION_INFO, *PCLUS_PARTITION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_PARTITION_INFO
 - clusapi/CLUS_PARTITION_INFO
 - PCLUS_PARTITION_INFO
 - clusapi/PCLUS_PARTITION_INFO
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
 - CLUS_PARTITION_INFO
---

# CLUS_PARTITION_INFO structure


## -description

Contains data describing a 
    <a href="/previous-versions/windows/desktop/mscs/s-gly">storage class resource</a> volume and file 
    system. It is used as the data member of a 
    <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a> structure and as the 
    return value of some <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> operations.

## -struct-fields

### -field dwFlags

Flags that describes the storage class resource, enumerated by the 
      <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-clusprop_piflags">CLUSPROP_PIFLAGS</a> enumeration.



#### CLUSPROP_PIFLAG_STICKY (0x00000001)

The drive letter is sticky.



#### CLUSPROP_PIFLAG_REMOVABLE (0x00000002)

The storage class resource is removable.



#### CLUSPROP_PIFLAG_USABLE (0x00000004)

The storage class resource is formatted with a file system that is usable by the 
        <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>.



#### CLUSPROP_PIFLAG_DEFAULT_QUORUM (0x00000008)

The partition should be used to store quorum files if no partition is specified in the 
        <a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterquorumresource">SetClusterQuorumResource</a> function. For 
        <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resources, the smallest NTFS partition 
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
    <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a> 
     and can be returned by 
     <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-available-disks">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>.


#### Examples

See 
     <a href="/previous-versions/windows/desktop/mscs/creating-physical-disk-resources">Creating Physical Disk Resources</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-available-disks">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a>