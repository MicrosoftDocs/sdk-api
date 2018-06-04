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

# CLUSPROP_PIFLAGS enumeration


## -description


Represents disk partition information.  The enumeration flags identify certain properties of a disk partition, 
    which is a 
    <a href="s_gly.htm">storage class resource</a>.


## -enum-fields




### -field CLUSPROP_PIFLAG_STICKY

The drive letter is sticky.


### -field CLUSPROP_PIFLAG_REMOVABLE

The storage class resource is removable.


### -field CLUSPROP_PIFLAG_USABLE

The storage class resource is formatted with a file system that is usable by the 
      <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>.


### -field CLUSPROP_PIFLAG_DEFAULT_QUORUM

The partition should be used to store quorum files if no partition is specified in the 
      <a href="https://msdn.microsoft.com/1a00c09e-4470-4c02-807d-c559fd992066">SetClusterQuorumResource</a> function.


### -field CLUSPROP_PIFLAG_USABLE_FOR_CSV

The partition can be used in a cluster shared volume (CSV).

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported starting with Windows Server 2012.




### -field CLUSPROP_PIFLAG_ENCRYPTION_ENABLED

The partition uses BitLocker encryption.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported starting with Windows Server 2016.




### -field CLUSPROP_PIFLAG_UNKNOWN

The partition uses an unknown file system type.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported starting with Windows Server 2012 R2 with KB 3093899.




## -remarks



For <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources, the smallest NTFS partition 
     larger than 50 MB automatically receives the <b>CLUSPROP_PIFLAG_DEFAULT_QUORUM</b> flag.




## -see-also




<a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/b1343a04-b8bd-469a-a620-985eeb89401c">CLUSPROP_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/d061bcb5-7c4c-4d07-9cdf-fa9f7ac34b3c">CLUS_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/19a69c92-495c-486d-9f42-6b0531dfb992">Flags Property of the ClusPartition Object</a>
 

 

