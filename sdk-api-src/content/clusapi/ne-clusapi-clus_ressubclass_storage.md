---
UID: NE:clusapi.CLUS_RESSUBCLASS_STORAGE
title: CLUS_RESSUBCLASS_STORAGE (clusapi.h)
description: Identifies a resource subclass that manages a shared bus.
helpviewer_keywords: ["CLUS_RESSUBCLASS_STORAGE","CLUS_RESSUBCLASS_STORAGE enumeration [Failover Cluster]","CLUS_RESSUBCLASS_STORAGE_DISK","CLUS_RESSUBCLASS_STORAGE_REPLICATION","CLUS_RESSUBCLASS_STORAGE_SHARED_BUS","clusapi/CLUS_RESSUBCLASS_STORAGE","clusapi/CLUS_RESSUBCLASS_STORAGE_DISK","clusapi/CLUS_RESSUBCLASS_STORAGE_REPLICATION","clusapi/CLUS_RESSUBCLASS_STORAGE_SHARED_BUS","msclus/CLUS_RESSUBCLASS_STORAGE","msclus/CLUS_RESSUBCLASS_STORAGE_DISK","msclus/CLUS_RESSUBCLASS_STORAGE_REPLICATION","msclus/CLUS_RESSUBCLASS_STORAGE_SHARED_BUS","mscs.clus_ressubclass_storage"]
old-location: mscs\clus_ressubclass_storage.htm
tech.root: MsCS
ms.assetid: 10e2fe05-ea17-4f9d-a26d-eed6aa3abb04
ms.date: 12/05/2018
ms.keywords: CLUS_RESSUBCLASS_STORAGE, CLUS_RESSUBCLASS_STORAGE enumeration [Failover Cluster], CLUS_RESSUBCLASS_STORAGE_DISK, CLUS_RESSUBCLASS_STORAGE_REPLICATION, CLUS_RESSUBCLASS_STORAGE_SHARED_BUS, clusapi/CLUS_RESSUBCLASS_STORAGE, clusapi/CLUS_RESSUBCLASS_STORAGE_DISK, clusapi/CLUS_RESSUBCLASS_STORAGE_REPLICATION, clusapi/CLUS_RESSUBCLASS_STORAGE_SHARED_BUS, msclus/CLUS_RESSUBCLASS_STORAGE, msclus/CLUS_RESSUBCLASS_STORAGE_DISK, msclus/CLUS_RESSUBCLASS_STORAGE_REPLICATION, msclus/CLUS_RESSUBCLASS_STORAGE_SHARED_BUS, mscs.clus_ressubclass_storage
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
req.typenames: CLUS_RESSUBCLASS_STORAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_RESSUBCLASS_STORAGE
 - clusapi/CLUS_RESSUBCLASS_STORAGE
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
 - CLUS_RESSUBCLASS_STORAGE
---

# CLUS_RESSUBCLASS_STORAGE enumeration


## -description

Identifies a resource subclass that manages a shared bus.

## -enum-fields

### -field CLUS_RESSUBCLASS_STORAGE_SHARED_BUS:0x80000000

Identifies a resource subclass that manages a shared bus. The 
      <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> function with the 
      <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      information for a resource subclass.

### -field CLUS_RESSUBCLASS_STORAGE_DISK:0x40000000

Identifies a resource subclass that manages a disk.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not supported before Windows Server 2012 R2.

### -field CLUS_RESSUBCLASS_STORAGE_REPLICATION:0x10000000

Identifies a resource subclass that manages storage replication.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not supported before Windows Server 2016.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>
