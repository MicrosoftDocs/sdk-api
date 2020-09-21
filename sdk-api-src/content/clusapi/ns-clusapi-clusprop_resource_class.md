---
UID: NS:clusapi.CLUSPROP_RESOURCE_CLASS
title: CLUSPROP_RESOURCE_CLASS (clusapi.h)
description: Describes a resource class.
helpviewer_keywords: ["*PCLUSPROP_RESOURCE_CLASS","CLUSPROP_RESOURCE_CLASS","CLUSPROP_RESOURCE_CLASS structure [Failover Cluster]","CLUS_RESCLASS_NETWORK","CLUS_RESCLASS_STORAGE","CLUS_RESCLASS_UNKNOWN","CLUS_RESCLASS_USER","PCLUSPROP_RESOURCE_CLASS","PCLUSPROP_RESOURCE_CLASS structure pointer [Failover Cluster]","_wolf_clusprop_resource_class","clusapi/CLUSPROP_RESOURCE_CLASS","clusapi/PCLUSPROP_RESOURCE_CLASS","mscs.clusprop_resource_class"]
old-location: mscs\clusprop_resource_class.htm
tech.root: MsCS
ms.assetid: 9ec01908-3765-4e95-a9d3-fdf6daa5f64d
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_RESOURCE_CLASS, CLUSPROP_RESOURCE_CLASS, CLUSPROP_RESOURCE_CLASS structure [Failover Cluster], CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, PCLUSPROP_RESOURCE_CLASS, PCLUSPROP_RESOURCE_CLASS structure pointer [Failover Cluster], _wolf_clusprop_resource_class, clusapi/CLUSPROP_RESOURCE_CLASS, clusapi/PCLUSPROP_RESOURCE_CLASS, mscs.clusprop_resource_class'
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
req.typenames: CLUSPROP_RESOURCE_CLASS, *PCLUSPROP_RESOURCE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_RESOURCE_CLASS
 - clusapi/CLUSPROP_RESOURCE_CLASS
 - PCLUSPROP_RESOURCE_CLASS
 - clusapi/PCLUSPROP_RESOURCE_CLASS
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
 - CLUSPROP_RESOURCE_CLASS
---

# CLUSPROP_RESOURCE_CLASS structure


## -description

Describes a resource class. It is used as an entry in a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the resource class value.</li>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_class">CLUSTER_RESOURCE_CLASS</a> value describing the 
     resource class. <b>CLUSTER_RESOURCE_CLASS</b> is an 
     enumeration defined in ClusAPI.h.</li>
</ul>

## -struct-fields

### -field rc

Resource class described with one of these values enumerated by the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_class">CLUSTER_RESOURCE_CLASS</a> enumeration.



#### CLUS_RESCLASS_UNKNOWN (0)

Resource class is unknown.



#### CLUS_RESCLASS_STORAGE (1)


<a href="/previous-versions/windows/desktop/mscs/resources">Resource</a> is a storage device, such as a 
         <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resource.



#### CLUS_RESCLASS_NETWORK (2)


<a href="/previous-versions/windows/desktop/mscs/resources">Resource</a> is a 
         <a href="/previous-versions/windows/desktop/mscs/n-gly">network</a> device.



#### CLUS_RESCLASS_USER (32768)

Resource belongs to a user-defined class. <b>CLUS_RESCLASS_USER</b> specifies the 
         beginning of the range for user-defined resource classes.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_RESCLASS</b> (0x00020002) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>rc</b> member.

## -remarks

A resource class identifies resources of similar capability. A 
     <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> that defines its own resource class should 
     provide a unique identifier for the class that is set to a value greater than 
     <b>CLUS_RESCLASS_USER</b>. <b>CLUS_RESCLASS_USER</b> specifies the 
     beginning for user-defined resource class identifiers.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_class">CLUSTER_RESOURCE_CLASS</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>