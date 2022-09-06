---
UID: NE:msclus.CLUS_RESSUBCLASS_NETWORK
title: CLUS_RESSUBCLASS_NETWORK (msclus.h)
description: Identifies a resource subclass that manages an IP address provider.
helpviewer_keywords: ["CLUS_RESSUBCLASS_NETWORK","CLUS_RESSUBCLASS_NETWORK enumeration [Failover Cluster]","CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL","clusapi/CLUS_RESSUBCLASS_NETWORK","clusapi/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL","msclus/CLUS_RESSUBCLASS_NETWORK","msclus/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL","mscs.clus_ressubclass_network"]
old-location: mscs\clus_ressubclass_network.htm
tech.root: MsCS
ms.assetid: 1dea2545-f0d4-4730-87af-19de135c1640
ms.date: 12/05/2018
ms.keywords: CLUS_RESSUBCLASS_NETWORK, CLUS_RESSUBCLASS_NETWORK enumeration [Failover Cluster], CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, clusapi/CLUS_RESSUBCLASS_NETWORK, clusapi/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, msclus/CLUS_RESSUBCLASS_NETWORK, msclus/CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL, mscs.clus_ressubclass_network
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
req.typenames: CLUS_RESSUBCLASS_NETWORK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_RESSUBCLASS_NETWORK
 - msclus/CLUS_RESSUBCLASS_NETWORK
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
 - CLUS_RESSUBCLASS_NETWORK
---

# CLUS_RESSUBCLASS_NETWORK enumeration


## -description

Identifies a resource subclass that manages an IP address provider.

## -enum-fields

### -field CLUS_RESSUBCLASS_NETWORK_INTERNET_PROTOCOL:0x80000000

Identifies a resource subclass that manages an IP address provider. The 
      <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> function with the 
      <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      this information.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>
