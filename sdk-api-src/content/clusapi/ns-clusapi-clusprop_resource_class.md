---
UID: NS:clusapi.CLUSPROP_RESOURCE_CLASS
title: CLUSPROP_RESOURCE_CLASS
author: windows-sdk-content
description: Describes a resource class.
old-location: mscs\clusprop_resource_class.htm
old-project: MsCS
ms.assetid: 9ec01908-3765-4e95-a9d3-fdf6daa5f64d
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PCLUSPROP_RESOURCE_CLASS, CLUSPROP_RESOURCE_CLASS, CLUSPROP_RESOURCE_CLASS structure [Failover Cluster], CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, PCLUSPROP_RESOURCE_CLASS, PCLUSPROP_RESOURCE_CLASS structure pointer [Failover Cluster], _wolf_clusprop_resource_class, clusapi/CLUSPROP_RESOURCE_CLASS, clusapi/PCLUSPROP_RESOURCE_CLASS, mscs.clusprop_resource_class"
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
tech.root: 
req.typenames: CLUSPROP_RESOURCE_CLASS, *PCLUSPROP_RESOURCE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_RESOURCE_CLASS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSPROP_RESOURCE_CLASS structure


## -description


Describes a resource class. It is used as an entry in a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the resource class value.</li>
<li>A <a href="https://msdn.microsoft.com/65168256-f097-48a5-9e86-ec419ccb13bd">CLUSTER_RESOURCE_CLASS</a> value describing the 
     resource class. <b>CLUSTER_RESOURCE_CLASS</b> is an 
     enumeration defined in ClusAPI.h.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> members are listed 
    explicitly:


## -struct-fields




### -field rc

Resource class described with one of these values enumerated by the 
       <a href="https://msdn.microsoft.com/65168256-f097-48a5-9e86-ec419ccb13bd">CLUSTER_RESOURCE_CLASS</a> enumeration.



#### CLUS_RESCLASS_UNKNOWN (0)

Resource class is unknown.



#### CLUS_RESCLASS_STORAGE (1)


<a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">Resource</a> is a storage device, such as a 
         <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resource.



#### CLUS_RESCLASS_NETWORK (2)


<a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">Resource</a> is a 
         <a href="https://www.bing.com/search?q=network">network</a> device.



#### CLUS_RESCLASS_USER (32768)

Resource belongs to a user-defined class. <b>CLUS_RESCLASS_USER</b> specifies the 
         beginning of the range for user-defined resource classes.


### -field CLUSPROP_VALUE

 




#### - ;



#### Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
        of <b>CLUSPROP_SYNTAX_RESCLASS</b> (0x00020002).



#### cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
        the count of bytes in the <b>rc</b> member. Padding bytes are not included in the 
        count.


## -remarks



A resource class identifies resources of similar capability. A 
     <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> that defines its own resource class should 
     provide a unique identifier for the class that is set to a value greater than 
     <b>CLUS_RESCLASS_USER</b>. <b>CLUS_RESCLASS_USER</b> specifies the 
     beginning for user-defined resource class identifiers.




## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/65168256-f097-48a5-9e86-ec419ccb13bd">CLUSTER_RESOURCE_CLASS</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

