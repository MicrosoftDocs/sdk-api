---
UID: NE:msclus.CLUS_RESSUBCLASS
title: CLUS_RESSUBCLASS (msclus.h)
description: Identifies a resource subclass that manages a shared resource.
helpviewer_keywords: ["CLUS_RESSUBCLASS","CLUS_RESSUBCLASS enumeration [Failover Cluster]","CLUS_RESSUBCLASS_SHARED","_CLUS_RESSUBCLASS","_CLUS_RESSUBCLASS enumeration [Failover Cluster]","clusapi/CLUS_RESSUBCLASS","clusapi/CLUS_RESSUBCLASS_SHARED","clusapi/_CLUS_RESSUBCLASS","msclus/CLUS_RESSUBCLASS","msclus/CLUS_RESSUBCLASS_SHARED","msclus/_CLUS_RESSUBCLASS","mscs.clus_ressubclass"]
old-location: mscs\clus_ressubclass.htm
tech.root: MsCS
ms.assetid: 2e10a529-a12d-4259-a18a-be96471ab3a5
ms.date: 12/05/2018
ms.keywords: CLUS_RESSUBCLASS, CLUS_RESSUBCLASS enumeration [Failover Cluster], CLUS_RESSUBCLASS_SHARED, _CLUS_RESSUBCLASS, _CLUS_RESSUBCLASS enumeration [Failover Cluster], clusapi/CLUS_RESSUBCLASS, clusapi/CLUS_RESSUBCLASS_SHARED, clusapi/_CLUS_RESSUBCLASS, msclus/CLUS_RESSUBCLASS, msclus/CLUS_RESSUBCLASS_SHARED, msclus/_CLUS_RESSUBCLASS, mscs.clus_ressubclass
req.header: msclus.h
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
req.typenames: CLUS_RESSUBCLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_RESSUBCLASS
 - msclus/CLUS_RESSUBCLASS
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
 - CLUS_RESSUBCLASS
---

# CLUS_RESSUBCLASS enumeration


## -description

Identifies a resource subclass that manages a shared resource.

## -enum-fields

### -field CLUS_RESSUBCLASS_SHARED:0x80000000

Identifies a resource subclass that manages a shared resource, such as a disk on a shared SCSI bus. The 
      <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> function with the 
      <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      this information.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>
