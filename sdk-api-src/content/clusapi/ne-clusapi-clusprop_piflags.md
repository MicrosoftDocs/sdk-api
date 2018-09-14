---
UID: NE:clusapi.CLUSPROP_PIFLAGS
title: CLUSPROP_PIFLAGS
author: windows-sdk-content
description: Represents disk partition information. The enumeration flags identify certain properties of a disk partition, which is a storage class resource.
old-location: mscs\clusprop_piflags.htm
tech.root: mscs
ms.assetid: 54597c05-57af-49ad-96e0-171f09c45a65
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CLUSPROP_PIFLAGS, CLUSPROP_PIFLAGS enumeration [Failover Cluster], CLUSPROP_PIFLAG_DEFAULT_QUORUM, CLUSPROP_PIFLAG_ENCRYPTION_ENABLED, CLUSPROP_PIFLAG_REMOVABLE, CLUSPROP_PIFLAG_STICKY, CLUSPROP_PIFLAG_UNKNOWN, CLUSPROP_PIFLAG_USABLE, CLUSPROP_PIFLAG_USABLE_FOR_CSV, _CLUSPROP_PIFLAGS, _CLUSPROP_PIFLAGS enumeration [Failover Cluster], clusapi/CLUSPROP_PIFLAGS, clusapi/CLUSPROP_PIFLAG_DEFAULT_QUORUM, clusapi/CLUSPROP_PIFLAG_ENCRYPTION_ENABLED, clusapi/CLUSPROP_PIFLAG_REMOVABLE, clusapi/CLUSPROP_PIFLAG_STICKY, clusapi/CLUSPROP_PIFLAG_UNKNOWN, clusapi/CLUSPROP_PIFLAG_USABLE, clusapi/CLUSPROP_PIFLAG_USABLE_FOR_CSV, clusapi/_CLUSPROP_PIFLAGS, msclus/CLUSPROP_PIFLAGS, msclus/CLUSPROP_PIFLAG_DEFAULT_QUORUM, msclus/CLUSPROP_PIFLAG_ENCRYPTION_ENABLED, msclus/CLUSPROP_PIFLAG_REMOVABLE, msclus/CLUSPROP_PIFLAG_STICKY, msclus/CLUSPROP_PIFLAG_UNKNOWN, msclus/CLUSPROP_PIFLAG_USABLE, msclus/CLUSPROP_PIFLAG_USABLE_FOR_CSV, msclus/_CLUSPROP_PIFLAGS, mscs.clusprop_piflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
 - MsClus.h
api_name:
 - CLUSPROP_PIFLAGS
product: Windows
targetos: Windows
req.typenames: CLUSPROP_PIFLAGS
req.redist: 
---

# CLUSPROP_PIFLAGS enumeration


## -description


Represents disk partition information.  The enumeration flags identify certain properties of a disk partition, 
    which is a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">storage class resource</a>.


## -enum-fields




### -field CLUSPROP_PIFLAG_STICKY

The drive letter is sticky.


### -field CLUSPROP_PIFLAG_REMOVABLE

The storage class resource is removable.


### -field CLUSPROP_PIFLAG_USABLE

The storage class resource is formatted with a file system that is usable by the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a>.


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



For <a href="https://msdn.microsoft.com/en-us/library/Aa371789(v=VS.85).aspx">Physical Disk</a> resources, the smallest NTFS partition 
     larger than 50 MB automatically receives the <b>CLUSPROP_PIFLAG_DEFAULT_QUORUM</b> flag.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368381(v=VS.85).aspx">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/b1343a04-b8bd-469a-a620-985eeb89401c">CLUSPROP_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/d061bcb5-7c4c-4d07-9cdf-fa9f7ac34b3c">CLUS_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368118(v=VS.85).aspx">Flags Property of the ClusPartition Object</a>
 

 

