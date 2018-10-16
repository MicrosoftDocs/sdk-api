---
UID: NS:clusapi.CLUSPROP_RESOURCE_CLASS_INFO
title: CLUSPROP_RESOURCE_CLASS_INFO
author: windows-sdk-content
description: Describes information relating to a resource class.
old-location: mscs\clusprop_resource_class_info.htm
tech.root: mscs
ms.assetid: 449f297e-6207-446e-ac80-03145c44d671
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCLUSPROP_RESOURCE_CLASS_INFO, CLUSPROP_RESOURCE_CLASS_INFO, CLUSPROP_RESOURCE_CLASS_INFO structure [Failover Cluster], CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, PCLUSPROP_RESOURCE_CLASS_INFO, PCLUSPROP_RESOURCE_CLASS_INFO structure pointer [Failover Cluster], _wolf_clusprop_resource_class_info, clusapi/CLUSPROP_RESOURCE_CLASS_INFO, clusapi/PCLUSPROP_RESOURCE_CLASS_INFO, mscs.clusprop_resource_class_info"
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
 - CLUSPROP_RESOURCE_CLASS_INFO
product: Windows
targetos: Windows
req.typenames: CLUSPROP_RESOURCE_CLASS_INFO, *PCLUSPROP_RESOURCE_CLASS_INFO
req.redist: 
---

# CLUSPROP_RESOURCE_CLASS_INFO structure


## -description


Describes information relating to a resource class. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure 
     describing the resource class and subclass of the resource.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> and 
    <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> members are listed 
    explicitly.


## -struct-fields




### -field CLUSPROP_VALUE

 


### -field CLUS_RESOURCE_CLASS_INFO

 




#### - DUMMYUNIONNAME



#### DUMMYSTRUCTNAME



##### DUMMYUNIONNAME



###### dw

Member of the 
         <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure that 
         describes the resource class as a numeric value.



###### rc

Member of the 
         <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure that 
         describes the resource class with one of the following values.



####### CLUS_RESCLASS_UNKNOWN

Resource class is unknown.



####### CLUS_RESCLASS_STORAGE

Resource is a storage device, such as a 
           <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resource.



####### CLUS_RESCLASS_USER

Resource belongs to a user-defined class. <b>CLUS_RESCLASS_USER</b> specifies the 
           beginning of the range for user-defined resource classes.



##### SubClass

Member of the <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> 
         structure that further describes the resource class. The following value is valid for 
         <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources:

<b>CLUS_RESSUBCLASS_SHARED</b>

Setting <b>SubClass</b> to <b>CLUS_RESSUBCLASS_SHARED</b> 
         indicates that the resource manages a shared resource such as a disk on a shared SCSI bus.



#### li

Member of the <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> 
       structure that describes the resource class and subclass as a <b>ULARGE_INTEGER</b> value 
       with a low <b>DWORD</b> and a high <b>DWORD</b>.


#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing 
      the format and type of the data in the 
      <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure.


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
      the count of bytes in the 
      <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure. Padding 
      bytes are not included in the count.


## -remarks



A resource class identifies resources of similar capability. A 
    <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> that defines its own resource class should 
    provide a unique identifier for the class that is set to a value greater than 
    <b>CLUS_RESCLASS_USER</b>. <b>CLUS_RESCLASS_USER</b> specifies the beginning 
    for user-defined resource class identifiers.




## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

