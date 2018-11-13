---
UID: NS:clusapi.CLUS_RESOURCE_CLASS_INFO
title: CLUS_RESOURCE_CLASS_INFO
author: windows-sdk-content
description: Contains resource class data. It is used as the data member of a CLUSPROP_RESOURCE_CLASS_INFO structure and as the return value of some control code operations.
old-location: mscs\clus_resource_class_info.htm
tech.root: mscs
ms.assetid: b8b6c479-2e35-4cc9-b864-d495c3bded25
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: "*PCLUS_RESOURCE_CLASS_INFO, CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, CLUS_RESOURCE_CLASS_INFO, CLUS_RESOURCE_CLASS_INFO structure [Failover Cluster], CLUS_RESSUBCLASS_SHARED, PCLUS_RESOURCE_CLASS_INFO, PCLUS_RESOURCE_CLASS_INFO structure pointer [Failover Cluster], _wolf_clus_resource_class_info, clusapi/CLUS_RESOURCE_CLASS_INFO, clusapi/PCLUS_RESOURCE_CLASS_INFO, mscs.clus_resource_class_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_RESOURCE_CLASS_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_RESOURCE_CLASS_INFO, *PCLUS_RESOURCE_CLASS_INFO
req.redist: 
---

# CLUS_RESOURCE_CLASS_INFO structure


## -description


Contains resource class data. It is used as the data member of a 
    <a href="https://msdn.microsoft.com/449f297e-6207-446e-ac80-03145c44d671">CLUSPROP_RESOURCE_CLASS_INFO</a> structure and 
    as the return value of some <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> operations.


## -struct-fields




### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DUMMYUNIONNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DUMMYUNIONNAME.dw

Provides another way to access the resource class data.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc

Resource class described with one of the following values enumerated from the 
          <a href="https://msdn.microsoft.com/65168256-f097-48a5-9e86-ec419ccb13bd">CLUSTER_RESOURCE_CLASS</a> enumeration.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_UNKNOWN (0)

Resource class is unknown.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_STORAGE (1)

Resource is a storage device, such as a 
            <a href="p_gly.htm">Physical Disk resource</a>.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_NETWORK (2)

Resource is a <a href="n_gly.htm">network</a> device.



####### DUMMYSTRUCTNAME.DUMMYUNIONNAME.rc.CLUS_RESCLASS_USER (32768 (0x8000))

Resource classes beginning at this value are user-defined.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.SubClass

A mask value that further describes the resource class. The following value is valid for storage class 
         resources such as <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources.



###### DUMMYSTRUCTNAME.SubClass.CLUS_RESSUBCLASS_SHARED (0x80000000)

Indicates that the resource manages a shared resource such as a disk on a shared 
           <a href="s_gly.htm">SCSI</a> bus.


### -field DUMMYUNIONNAME.li

Resource class and subclass described as a <b>ULARGE_INTEGER</b> value with a low 
        <b>DWORD</b> and a high <b>DWORD</b>.


## -remarks



A resource class identifies resources of similar capability. A 
     <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> that defines its own resource class should 
     provide a unique identifier for the class that is set to a value greater than 
     <b>CLUS_RESCLASS_USER</b>. <b>CLUS_RESCLASS_USER</b> specifies the 
     beginning for user-defined resource class identifiers.

A <b>CLUS_RESOURCE_CLASS_INFO</b> structure is 
     returned by <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
     and is returned by 
     <a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="https://msdn.microsoft.com/db811070-9de6-4368-b9b5-ac17259d68a1">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/db811070-9de6-4368-b9b5-ac17259d68a1">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/449f297e-6207-446e-ac80-03145c44d671">CLUSPROP_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/65168256-f097-48a5-9e86-ec419ccb13bd">CLUSTER_RESOURCE_CLASS</a>



<a href="https://msdn.microsoft.com/2e10a529-a12d-4259-a18a-be96471ab3a5">CLUS_RESSUBCLASS</a>



<a href="https://msdn.microsoft.com/1dea2545-f0d4-4730-87af-19de135c1640">CLUS_RESSUBCLASS_NETWORK</a>



<a href="https://msdn.microsoft.com/10e2fe05-ea17-4f9d-a26d-eed6aa3abb04">CLUS_RESSUBCLASS_STORAGE</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a>
 

 

