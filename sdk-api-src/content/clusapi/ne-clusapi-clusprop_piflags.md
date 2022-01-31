---
UID: NE:clusapi.CLUSPROP_PIFLAGS
title: CLUSPROP_PIFLAGS (clusapi.h)
description: Represents disk partition information. The enumeration flags identify certain properties of a disk partition, which is a storage class resource.
helpviewer_keywords: ["CLUSPROP_PIFLAGS","CLUSPROP_PIFLAGS enumeration [Failover Cluster]","CLUSPROP_PIFLAG_DEFAULT_QUORUM","CLUSPROP_PIFLAG_ENCRYPTION_ENABLED","CLUSPROP_PIFLAG_REMOVABLE","CLUSPROP_PIFLAG_STICKY","CLUSPROP_PIFLAG_UNKNOWN","CLUSPROP_PIFLAG_USABLE","CLUSPROP_PIFLAG_USABLE_FOR_CSV","_CLUSPROP_PIFLAGS","_CLUSPROP_PIFLAGS enumeration [Failover Cluster]","clusapi/CLUSPROP_PIFLAGS","clusapi/CLUSPROP_PIFLAG_DEFAULT_QUORUM","clusapi/CLUSPROP_PIFLAG_ENCRYPTION_ENABLED","clusapi/CLUSPROP_PIFLAG_REMOVABLE","clusapi/CLUSPROP_PIFLAG_STICKY","clusapi/CLUSPROP_PIFLAG_UNKNOWN","clusapi/CLUSPROP_PIFLAG_USABLE","clusapi/CLUSPROP_PIFLAG_USABLE_FOR_CSV","clusapi/_CLUSPROP_PIFLAGS","msclus/CLUSPROP_PIFLAGS","msclus/CLUSPROP_PIFLAG_DEFAULT_QUORUM","msclus/CLUSPROP_PIFLAG_ENCRYPTION_ENABLED","msclus/CLUSPROP_PIFLAG_REMOVABLE","msclus/CLUSPROP_PIFLAG_STICKY","msclus/CLUSPROP_PIFLAG_UNKNOWN","msclus/CLUSPROP_PIFLAG_USABLE","msclus/CLUSPROP_PIFLAG_USABLE_FOR_CSV","msclus/_CLUSPROP_PIFLAGS","mscs.clusprop_piflags"]
old-location: mscs\clusprop_piflags.htm
tech.root: MsCS
ms.assetid: 54597c05-57af-49ad-96e0-171f09c45a65
ms.date: 12/05/2018
ms.keywords: CLUSPROP_PIFLAGS, CLUSPROP_PIFLAGS enumeration [Failover Cluster], CLUSPROP_PIFLAG_DEFAULT_QUORUM, CLUSPROP_PIFLAG_ENCRYPTION_ENABLED, CLUSPROP_PIFLAG_REMOVABLE, CLUSPROP_PIFLAG_STICKY, CLUSPROP_PIFLAG_UNKNOWN, CLUSPROP_PIFLAG_USABLE, CLUSPROP_PIFLAG_USABLE_FOR_CSV, _CLUSPROP_PIFLAGS, _CLUSPROP_PIFLAGS enumeration [Failover Cluster], clusapi/CLUSPROP_PIFLAGS, clusapi/CLUSPROP_PIFLAG_DEFAULT_QUORUM, clusapi/CLUSPROP_PIFLAG_ENCRYPTION_ENABLED, clusapi/CLUSPROP_PIFLAG_REMOVABLE, clusapi/CLUSPROP_PIFLAG_STICKY, clusapi/CLUSPROP_PIFLAG_UNKNOWN, clusapi/CLUSPROP_PIFLAG_USABLE, clusapi/CLUSPROP_PIFLAG_USABLE_FOR_CSV, clusapi/_CLUSPROP_PIFLAGS, msclus/CLUSPROP_PIFLAGS, msclus/CLUSPROP_PIFLAG_DEFAULT_QUORUM, msclus/CLUSPROP_PIFLAG_ENCRYPTION_ENABLED, msclus/CLUSPROP_PIFLAG_REMOVABLE, msclus/CLUSPROP_PIFLAG_STICKY, msclus/CLUSPROP_PIFLAG_UNKNOWN, msclus/CLUSPROP_PIFLAG_USABLE, msclus/CLUSPROP_PIFLAG_USABLE_FOR_CSV, msclus/_CLUSPROP_PIFLAGS, mscs.clusprop_piflags
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
targetos: Windows
req.typenames: CLUSPROP_PIFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_PIFLAGS
 - clusapi/CLUSPROP_PIFLAGS
dev_langs:
 - c++
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
---

# CLUSPROP_PIFLAGS enumeration


## -description

Represents disk partition information.  The enumeration flags identify certain properties of a disk partition, 
    which is a 
    <a href="/previous-versions/windows/desktop/mscs/s-gly">storage class resource</a>.

## -enum-fields

### -field CLUSPROP_PIFLAG_STICKY:0x00000001

The drive letter is sticky.

### -field CLUSPROP_PIFLAG_REMOVABLE:0x00000002

The storage class resource is removable.

### -field CLUSPROP_PIFLAG_USABLE:0x00000004

The storage class resource is formatted with a file system that is usable by the 
      <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>.

### -field CLUSPROP_PIFLAG_DEFAULT_QUORUM:0x00000008

The partition should be used to store quorum files if no partition is specified in the 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterquorumresource">SetClusterQuorumResource</a> function.

### -field CLUSPROP_PIFLAG_USABLE_FOR_CSV:0x00000010

The partition can be used in a cluster shared volume (CSV).

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported starting with Windows Server 2012.

### -field CLUSPROP_PIFLAG_ENCRYPTION_ENABLED:0x00000020

The partition uses BitLocker encryption.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported starting with Windows Server 2016.

### -field CLUSPROP_PIFLAG_UNKNOWN:0x80000000

The partition uses an unknown file system type.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported starting with Windows Server 2012 R2 with KB 3093899.

## -remarks

For <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resources, the smallest NTFS partition 
     larger than 50 MB automatically receives the <b>CLUSPROP_PIFLAG_DEFAULT_QUORUM</b> flag.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex">CLUSPROP_PARTITION_INFO_EX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_partition_info">CLUS_PARTITION_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_partition_info_ex">CLUS_PARTITION_INFO_EX</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/mscs/cluspartition-flags">Flags Property of the ClusPartition Object</a>
