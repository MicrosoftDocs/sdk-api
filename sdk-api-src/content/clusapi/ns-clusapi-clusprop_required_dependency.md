---
UID: NS:clusapi.CLUSPROP_REQUIRED_DEPENDENCY
title: CLUSPROP_REQUIRED_DEPENDENCY (clusapi.h)
description: Describes a resource that is a required dependency of another resource. This union is used as a value in the value list returned from a CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES or CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES control code operation.
helpviewer_keywords: ["*PCLUSPROP_REQUIRED_DEPENDENCY","CLUSPROP_REQUIRED_DEPENDENCY","CLUSPROP_REQUIRED_DEPENDENCY structure [Failover Cluster]","CLUS_RESCLASS_NETWORK","CLUS_RESCLASS_STORAGE","CLUS_RESCLASS_UNKNOWN","CLUS_RESCLASS_USER","PCLUSPROP_REQUIRED_DEPENDENCY","PCLUSPROP_REQUIRED_DEPENDENCY structure pointer [Failover Cluster]","_wolf_clusprop_required_dependency","clusapi/CLUSPROP_REQUIRED_DEPENDENCY","clusapi/PCLUSPROP_REQUIRED_DEPENDENCY","mscs.clusprop_required_dependency"]
old-location: mscs\clusprop_required_dependency.htm
tech.root: MsCS
ms.assetid: dae7544d-31c0-4a4b-8acb-d652bae817dd
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_REQUIRED_DEPENDENCY, CLUSPROP_REQUIRED_DEPENDENCY, CLUSPROP_REQUIRED_DEPENDENCY structure [Failover Cluster], CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, PCLUSPROP_REQUIRED_DEPENDENCY, PCLUSPROP_REQUIRED_DEPENDENCY structure pointer [Failover Cluster], _wolf_clusprop_required_dependency, clusapi/CLUSPROP_REQUIRED_DEPENDENCY, clusapi/PCLUSPROP_REQUIRED_DEPENDENCY, mscs.clusprop_required_dependency'
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
req.typenames: CLUSPROP_REQUIRED_DEPENDENCY, *PCLUSPROP_REQUIRED_DEPENDENCY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_REQUIRED_DEPENDENCY
 - clusapi/CLUSPROP_REQUIRED_DEPENDENCY
 - PCLUSPROP_REQUIRED_DEPENDENCY
 - clusapi/PCLUSPROP_REQUIRED_DEPENDENCY
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
 - CLUSPROP_REQUIRED_DEPENDENCY
---

# CLUSPROP_REQUIRED_DEPENDENCY structure


## -description

Describes a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> that is a required 
    <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependency</a> of another resource. This union is used as 
    a value in the <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> returned from a 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-required-dependencies">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a> or 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-required-dependencies">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>
<a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> operation.

## -struct-fields

### -field Value

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing whether the data 
       in the structure is a resource class or resource type name.

### -field ResClass

Resource class upon which a resource must depend. One of the following values are valid.



#### CLUS_RESCLASS_UNKNOWN (0)

A resource has a dependency on a resource of an unknown class.



#### CLUS_RESCLASS_STORAGE (1)

A resource has a dependency on a storage device, such as a 
         <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resource.



#### CLUS_RESCLASS_NETWORK (2)

A resource has a dependency on a <a href="/previous-versions/windows/desktop/mscs/n-gly">network</a> device.



#### CLUS_RESCLASS_USER (32768)

A resource has a dependency on a resource belonging to a user-defined class. 
         <b>CLUS_RESCLASS_USER</b> specifies the beginning of the range for user-defined resource 
         classes.

### -field ResTypeName

<a href="/previous-versions/windows/desktop/mscs/resource-types">Resource type</a> upon which a resource must depend, such 
       as <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a>.

## -remarks

The <b>CLUSPROP_REQUIRED_DEPENDENCY</b> 
     structure describes mandatory dependencies. For example, a 
     <a href="/previous-versions/windows/desktop/mscs/print-spooler">Print Spooler</a> resource has required dependencies on a 
     storage device and a <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource. The first type of 
     dependency is described using a resource class; storage device resources belong to the 
     <b>CLUS_RESCLASS_STORAGE</b> resource class. The second type of dependency is described 
     using a resource type name, such as "Network Name". Therefore, when an application calls 
     <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> with the 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-required-dependencies">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a> 
     control code, a value list is returned with two entries: a 
     <b>CLUSPROP_REQUIRED_DEPENDENCY</b> structure 
     with the <b>ResClass</b> member set to <b>CLUS_RESCLASS_STORAGE</b>, and 
     a second <b>CLUSPROP_REQUIRED_DEPENDENCY</b> 
     structure with the <b>ResTypeName</b> member set to "Network Name".


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/creating-value-lists">Creating Value Lists</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-required-dependencies">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-required-dependencies">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>