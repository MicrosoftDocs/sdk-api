---
UID: NS:clusapi.CLUS_RESOURCE_CLASS_INFO
title: CLUS_RESOURCE_CLASS_INFO (clusapi.h)
description: Contains resource class data. It is used as the data member of a CLUSPROP_RESOURCE_CLASS_INFO structure and as the return value of some control code operations.
helpviewer_keywords: ["*PCLUS_RESOURCE_CLASS_INFO","CLUS_RESCLASS_NETWORK","CLUS_RESCLASS_STORAGE","CLUS_RESCLASS_UNKNOWN","CLUS_RESCLASS_USER","CLUS_RESOURCE_CLASS_INFO","CLUS_RESOURCE_CLASS_INFO structure [Failover Cluster]","CLUS_RESSUBCLASS_SHARED","PCLUS_RESOURCE_CLASS_INFO","PCLUS_RESOURCE_CLASS_INFO structure pointer [Failover Cluster]","_wolf_clus_resource_class_info","clusapi/CLUS_RESOURCE_CLASS_INFO","clusapi/PCLUS_RESOURCE_CLASS_INFO","mscs.clus_resource_class_info"]
old-location: mscs\clus_resource_class_info.htm
tech.root: MsCS
ms.assetid: b8b6c479-2e35-4cc9-b864-d495c3bded25
ms.date: 12/05/2018
ms.keywords: '*PCLUS_RESOURCE_CLASS_INFO, CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, CLUS_RESOURCE_CLASS_INFO, CLUS_RESOURCE_CLASS_INFO structure [Failover Cluster], CLUS_RESSUBCLASS_SHARED, PCLUS_RESOURCE_CLASS_INFO, PCLUS_RESOURCE_CLASS_INFO structure pointer [Failover Cluster], _wolf_clus_resource_class_info, clusapi/CLUS_RESOURCE_CLASS_INFO, clusapi/PCLUS_RESOURCE_CLASS_INFO, mscs.clus_resource_class_info'
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
req.typenames: CLUS_RESOURCE_CLASS_INFO, *PCLUS_RESOURCE_CLASS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_RESOURCE_CLASS_INFO
 - clusapi/CLUS_RESOURCE_CLASS_INFO
 - PCLUS_RESOURCE_CLASS_INFO
 - clusapi/PCLUS_RESOURCE_CLASS_INFO
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
 - CLUS_RESOURCE_CLASS_INFO
---

# CLUS_RESOURCE_CLASS_INFO structure


## -description

Contains resource class data. It is used as the data member of a 
    <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class_info">CLUSPROP_RESOURCE_CLASS_INFO</a> structure and 
    as the return value of some <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> operations.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DUMMYUNIONNAME.dw

Provides another way to access the resource class data.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc

Resource class described with one of the following values enumerated from the 
          <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_class">CLUSTER_RESOURCE_CLASS</a> enumeration.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_UNKNOWN (0)

Resource class is unknown.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_STORAGE (1)

Resource is a storage device, such as a 
            <a href="/previous-versions/windows/desktop/mscs/p-gly">Physical Disk resource</a>.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_NETWORK (2)

Resource is a <a href="/previous-versions/windows/desktop/mscs/n-gly">network</a> device.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_USER (32768 (0x8000))

Resource classes beginning at this value are user-defined.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.SubClass

A mask value that further describes the resource class. The following value is valid for storage class 
         resources such as <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resources.



###### DUMMYSTRUCTNAME.SubClass.CLUS_RESSUBCLASS_SHARED (0x80000000)

Indicates that the resource manages a shared resource such as a disk on a shared 
           <a href="/previous-versions/windows/desktop/mscs/s-gly">SCSI</a> bus.

### -field DUMMYUNIONNAME.li

Resource class and subclass described as a <b>ULARGE_INTEGER</b> value with a low 
        <b>DWORD</b> and a high <b>DWORD</b>.

## -remarks

A resource class identifies resources of similar capability. A 
     <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> that defines its own resource class should 
     provide a unique identifier for the class that is set to a value greater than 
     <b>CLUS_RESCLASS_USER</b>. <b>CLUS_RESCLASS_USER</b> specifies the 
     beginning for user-defined resource class identifiers.

A <b>CLUS_RESOURCE_CLASS_INFO</b> structure is 
     returned by <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
     and is returned by 
     <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-class-info">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-class-info">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class_info">CLUSPROP_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_class">CLUSTER_RESOURCE_CLASS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-clus_ressubclass">CLUS_RESSUBCLASS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-clus_ressubclass_network">CLUS_RESSUBCLASS_NETWORK</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-clus_ressubclass_storage">CLUS_RESSUBCLASS_STORAGE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a>