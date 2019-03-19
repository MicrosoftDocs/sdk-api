---
UID: NS:clusapi.CLUSPROP_RESOURCE_CLASS_INFO
title: CLUSPROP_RESOURCE_CLASS_INFO (clusapi.h)
author: windows-sdk-content
description: Describes information relating to a resource class.
old-location: mscs\clusprop_resource_class_info.htm
tech.root: MsCS
ms.assetid: 449f297e-6207-446e-ac80-03145c44d671
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUSPROP_RESOURCE_CLASS_INFO, CLUSPROP_RESOURCE_CLASS_INFO, CLUSPROP_RESOURCE_CLASS_INFO structure [Failover Cluster], PCLUSPROP_RESOURCE_CLASS_INFO, PCLUSPROP_RESOURCE_CLASS_INFO structure pointer [Failover Cluster], _wolf_clusprop_resource_class_info, clusapi/CLUSPROP_RESOURCE_CLASS_INFO, clusapi/PCLUSPROP_RESOURCE_CLASS_INFO, mscs.clusprop_resource_class_info"
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
</ul>

## -struct-fields




### -field CLUSPROP_VALUE


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_RESOURCE_CLASS_INFO</b> member. Padding 
      bytes are not included in the count.


### -field CLUS_RESOURCE_CLASS_INFO


<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure.


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
 

 

