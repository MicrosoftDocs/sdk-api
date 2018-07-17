---
UID: NS:cfgmgr32.Mem_Resource_s
title: Mem_Resource_s
author: windows-sdk-content
description: The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
old-location: devinst\mem_resource.htm
old-project: devinst
ms.assetid: 42ecd736-abd3-4ac8-82bb-6bb69af1d96d
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: "*PMEM_RESOURCE, MEM_RESOURCE, MEM_RESOURCE structure [Device and Driver Installation], Mem_Resource_s, PMEM_RESOURCE, PMEM_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/MEM_RESOURCE, cfgmgr32/PMEM_RESOURCE, cfgmgrst_ab2f2f67-e38b-45b4-9b63-617d730f8cc8.xml, devinst.mem_resource"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MEM_RESOURCE, *PMEM_RESOURCE
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
req.lib: 
req.dll: 
req.irql: 
---

# Mem_Resource_s structure


## -description


The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field MEM_Header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548716">MEM_DES</a> structure.


### -field MEM_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548722">MEM_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548716">MEM_DES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548722">MEM_RANGE</a>
 

 

