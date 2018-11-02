---
UID: NS:cfgmgr32.IRQ_Resource_32_s
title: IRQ_Resource_32_s
author: windows-sdk-content
description: The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance.
old-location: devinst\irq_resource.htm
tech.root: devinst
ms.assetid: 448298d1-2583-47d5-b393-e6c8e59da64e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PIRQ_RESOURCE_32, IRQ_RESOURCE, IRQ_RESOURCE structure [Device and Driver Installation], IRQ_RESOURCE_32, IRQ_Resource_32_s, PIRQ_RESOURCE, PIRQ_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/IRQ_RESOURCE, cfgmgr32/PIRQ_RESOURCE, cfgmgrst_7eed527c-01ea-417a-b408-3239701cd988.xml, devinst.irq_resource"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cfgmgr32.h
api_name:
 - IRQ_RESOURCE
product: Windows
targetos: Windows
req.typenames: IRQ_RESOURCE_32, *PIRQ_RESOURCE_32
req.redist: 
---

# IRQ_Resource_32_s structure


## -description


The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


## -struct-fields




### -field IRQ_Header

An <a href="https://msdn.microsoft.com/fa8b8d96-6642-4f5a-b65c-0c7470340251">IRQ_DES</a> structure.


### -field IRQ_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

An <a href="https://msdn.microsoft.com/973834cc-0798-414f-a937-5ab14c214559">IRQ_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/fa8b8d96-6642-4f5a-b65c-0c7470340251">IRQ_DES</a>



<a href="https://msdn.microsoft.com/973834cc-0798-414f-a937-5ab14c214559">IRQ_RANGE</a>
 

 

