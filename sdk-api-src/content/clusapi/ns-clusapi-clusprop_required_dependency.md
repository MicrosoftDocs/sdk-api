---
UID: NS:clusapi.CLUSPROP_REQUIRED_DEPENDENCY
title: CLUSPROP_REQUIRED_DEPENDENCY
author: windows-driver-content
description: Describes a resource that is a required dependency of another resource. This union is used as a value in the value list returned from a CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES or CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES control code operation.
old-location: mscs\clusprop_required_dependency.htm
old-project: MsCS
ms.assetid: dae7544d-31c0-4a4b-8acb-d652bae817dd
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PCLUSPROP_REQUIRED_DEPENDENCY, CLUSPROP_REQUIRED_DEPENDENCY, CLUSPROP_REQUIRED_DEPENDENCY structure [Failover Cluster], CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, PCLUSPROP_REQUIRED_DEPENDENCY, PCLUSPROP_REQUIRED_DEPENDENCY structure pointer [Failover Cluster], _wolf_clusprop_required_dependency, clusapi/CLUSPROP_REQUIRED_DEPENDENCY, clusapi/PCLUSPROP_REQUIRED_DEPENDENCY, mscs.clusprop_required_dependency"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CLUSPROP_REQUIRED_DEPENDENCY, *PCLUSPROP_REQUIRED_DEPENDENCY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
api_name:
-	CLUSPROP_REQUIRED_DEPENDENCY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSPROP_REQUIRED_DEPENDENCY structure


## -description


Describes a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> that is a required 
    <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> of another resource. This union is used as 
    a value in the <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> returned from a 
    <a href="https://msdn.microsoft.com/4bf78e9c-a6da-453c-a199-9ec73fc5dafe">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a> or 
    <a href="https://msdn.microsoft.com/01a1b0bc-e831-4535-b782-2a24bd6adf22">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>
<a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> operation.


## -struct-fields




### -field Value


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing whether the data 
       in the structure is a resource class or resource type name.


### -field ResClass

Resource class upon which a resource must depend. One of the following values are valid.



#### CLUS_RESCLASS_UNKNOWN (0)

A resource has a dependency on a resource of an unknown class.



#### CLUS_RESCLASS_STORAGE (1)

A resource has a dependency on a storage device, such as a 
         <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resource.



#### CLUS_RESCLASS_NETWORK (2)

A resource has a dependency on a <a href="n_gly.htm">network</a> device.



#### CLUS_RESCLASS_USER (32768)

A resource has a dependency on a resource belonging to a user-defined class. 
         <b>CLUS_RESCLASS_USER</b> specifies the beginning of the range for user-defined resource 
         classes.


### -field ResTypeName


<a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">Resource type</a> upon which a resource must depend, such 
       as <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a>.


## -remarks



The <b>CLUSPROP_REQUIRED_DEPENDENCY</b> 
     structure describes mandatory dependencies. For example, a 
     <a href="https://msdn.microsoft.com/f94ccac1-5223-4e96-b275-229bddfeb8df">Print Spooler</a> resource has required dependencies on a 
     storage device and a <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource. The first type of 
     dependency is described using a resource class; storage device resources belong to the 
     <b>CLUS_RESCLASS_STORAGE</b> resource class. The second type of dependency is described 
     using a resource type name, such as "Network Name". Therefore, when an application calls 
     <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> with the 
     <a href="https://msdn.microsoft.com/4bf78e9c-a6da-453c-a199-9ec73fc5dafe">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a> 
     control code, a value list is returned with two entries: a 
     <b>CLUSPROP_REQUIRED_DEPENDENCY</b> structure 
     with the <b>ResClass</b> member set to <b>CLUS_RESCLASS_STORAGE</b>, and 
     a second <b>CLUSPROP_REQUIRED_DEPENDENCY</b> 
     structure with the <b>ResTypeName</b> member set to "Network Name".


#### Examples

See <a href="https://msdn.microsoft.com/7af7f5a8-fe1f-4b2a-9332-fd2cefc18cc2">Creating Value Lists</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4bf78e9c-a6da-453c-a199-9ec73fc5dafe">CLUSCTL_RESOURCE_GET_REQUIRED_DEPENDENCIES</a>



<a href="https://msdn.microsoft.com/01a1b0bc-e831-4535-b782-2a24bd6adf22">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

