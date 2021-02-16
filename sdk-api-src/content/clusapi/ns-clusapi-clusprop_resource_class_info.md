---
UID: NS:clusapi.CLUSPROP_RESOURCE_CLASS_INFO
title: CLUSPROP_RESOURCE_CLASS_INFO (clusapi.h)
description: Describes information relating to a resource class.
helpviewer_keywords: ["*PCLUSPROP_RESOURCE_CLASS_INFO","CLUSPROP_RESOURCE_CLASS_INFO","CLUSPROP_RESOURCE_CLASS_INFO structure [Failover Cluster]","PCLUSPROP_RESOURCE_CLASS_INFO","PCLUSPROP_RESOURCE_CLASS_INFO structure pointer [Failover Cluster]","_wolf_clusprop_resource_class_info","clusapi/CLUSPROP_RESOURCE_CLASS_INFO","clusapi/PCLUSPROP_RESOURCE_CLASS_INFO","mscs.clusprop_resource_class_info"]
old-location: mscs\clusprop_resource_class_info.htm
tech.root: MsCS
ms.assetid: 449f297e-6207-446e-ac80-03145c44d671
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_RESOURCE_CLASS_INFO, CLUSPROP_RESOURCE_CLASS_INFO, CLUSPROP_RESOURCE_CLASS_INFO structure [Failover Cluster], PCLUSPROP_RESOURCE_CLASS_INFO, PCLUSPROP_RESOURCE_CLASS_INFO structure pointer [Failover Cluster], _wolf_clusprop_resource_class_info, clusapi/CLUSPROP_RESOURCE_CLASS_INFO, clusapi/PCLUSPROP_RESOURCE_CLASS_INFO, mscs.clusprop_resource_class_info'
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
req.typenames: CLUSPROP_RESOURCE_CLASS_INFO, *PCLUSPROP_RESOURCE_CLASS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_RESOURCE_CLASS_INFO
 - clusapi/CLUSPROP_RESOURCE_CLASS_INFO
 - PCLUSPROP_RESOURCE_CLASS_INFO
 - clusapi/PCLUSPROP_RESOURCE_CLASS_INFO
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
 - CLUSPROP_RESOURCE_CLASS_INFO
---

# CLUSPROP_RESOURCE_CLASS_INFO structure


## -description

Describes information relating to a resource class. It is used as an entry in a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure 
     describing the resource class and subclass of the resource.</li>
</ul>

## -struct-fields

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_RESOURCE_CLASS_INFO</b> member. Padding 
      bytes are not included in the count.

### -field CLUS_RESOURCE_CLASS_INFO

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure.

## -remarks

A resource class identifies resources of similar capability. A 
    <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> that defines its own resource class should 
    provide a unique identifier for the class that is set to a value greater than 
    <b>CLUS_RESCLASS_USER</b>. <b>CLUS_RESCLASS_USER</b> specifies the beginning 
    for user-defined resource class identifiers.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>