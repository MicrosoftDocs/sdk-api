---
UID: NS:cfgmgr32.Mem_Resource_s
title: MEM_RESOURCE
author: windows-sdk-content
description: The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
old-location: devinst\mem_resource.htm
tech.root: devinst
ms.assetid: 42ecd736-abd3-4ac8-82bb-6bb69af1d96d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMEM_RESOURCE, MEM_RESOURCE, MEM_RESOURCE structure [Device and Driver Installation], PMEM_RESOURCE, PMEM_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/MEM_RESOURCE, cfgmgr32/PMEM_RESOURCE, cfgmgrst_ab2f2f67-e38b-45b4-9b63-617d730f8cc8.xml, devinst.mem_resource"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - cfgmgr32.h
api_name:
 - MEM_RESOURCE
product: Windows
targetos: Windows
req.typenames: MEM_RESOURCE, *PMEM_RESOURCE
req.redist: 
---

# MEM_RESOURCE structure


## -description


The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


## -struct-fields




### -field MEM_Header

A <a href="https://msdn.microsoft.com/1a9ee8f2-fabe-4351-b11e-93f46e190d66">MEM_DES</a> structure.


### -field MEM_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

A <a href="https://msdn.microsoft.com/a31ae199-8f4a-4d1f-891c-f1dc11a4edde">MEM_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/1a9ee8f2-fabe-4351-b11e-93f46e190d66">MEM_DES</a>



<a href="https://msdn.microsoft.com/a31ae199-8f4a-4d1f-891c-f1dc11a4edde">MEM_RANGE</a>
 

 

