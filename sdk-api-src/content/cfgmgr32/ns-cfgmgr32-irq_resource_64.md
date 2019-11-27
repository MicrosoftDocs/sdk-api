---
UID: NS:cfgmgr32.IRQ_Resource_64_s
title: IRQ_RESOURCE_64 (cfgmgr32.h)

description: The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance.
old-location: devinst\irq_resource.htm
tech.root: devinst
ms.assetid: 448298d1-2583-47d5-b393-e6c8e59da64e

ms.date: 12/05/2018
ms.keywords: "*PIRQ_RESOURCE_64, IRQ_RESOURCE, IRQ_RESOURCE structure [Device and Driver Installation], IRQ_RESOURCE_64, PIRQ_RESOURCE, PIRQ_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/IRQ_RESOURCE, cfgmgr32/PIRQ_RESOURCE, cfgmgrst_7eed527c-01ea-417a-b408-3239701cd988.xml, devinst.irq_resource"
ms.topic: struct
f1_keywords: 
 - "cfgmgr32/IRQ_RESOURCE"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: IRQ_RESOURCE_64, *PIRQ_RESOURCE_64
req.redist: 
ms.custom: 19H1
---

# IRQ_RESOURCE_64 structure


## -description


The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.


## -struct-fields




### -field IRQ_Header

An [IRQ_DES](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_des_32)a> structure.


### -field IRQ_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

An [IRQ_RANGE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_range)a> array.


##### - IRQ_Data.For a resource list:

Zero.


##### - IRQ_Data.For a resource requirements list:

An [IRQ_RANGE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_range)a> array.


## -see-also




[IRQ_DES](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_des_32)a>



[IRQ_RANGE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_range)a>
 

 

