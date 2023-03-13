---
UID: NS:cfgmgr32.IRQ_Resource_32_s
title: IRQ_RESOURCE_32 (cfgmgr32.h)
description: The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. (32 bit)
helpviewer_keywords: ["*PIRQ_RESOURCE_32","IRQ_RESOURCE","IRQ_RESOURCE structure [Device and Driver Installation]","IRQ_RESOURCE_32","PIRQ_RESOURCE","PIRQ_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/IRQ_RESOURCE","cfgmgr32/PIRQ_RESOURCE","cfgmgrst_7eed527c-01ea-417a-b408-3239701cd988.xml","devinst.irq_resource"]
old-location: devinst\irq_resource.htm
tech.root: devinst
ms.assetid: 448298d1-2583-47d5-b393-e6c8e59da64e
ms.date: 12/05/2018
ms.keywords: '*PIRQ_RESOURCE_32, IRQ_RESOURCE, IRQ_RESOURCE structure [Device and Driver Installation], IRQ_RESOURCE_32, PIRQ_RESOURCE, PIRQ_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/IRQ_RESOURCE, cfgmgr32/PIRQ_RESOURCE, cfgmgrst_7eed527c-01ea-417a-b408-3239701cd988.xml, devinst.irq_resource'
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
targetos: Windows
req.typenames: IRQ_RESOURCE_32, *PIRQ_RESOURCE_32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRQ_Resource_32_s
 - cfgmgr32/IRQ_Resource_32_s
 - PIRQ_RESOURCE_32
 - cfgmgr32/PIRQ_RESOURCE_32
 - IRQ_RESOURCE_32
 - cfgmgr32/IRQ_RESOURCE_32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cfgmgr32.h
api_name:
 - IRQ_RESOURCE
---

# IRQ_RESOURCE_32 structure


## -description

The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field IRQ_Header

An [IRQ_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_des_32) structure.

### -field IRQ_Data

#### For a resource list:

Zero.



#### For a resource requirements list:

An [IRQ_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_range) array.

## -see-also

[IRQ_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_des_32)



[IRQ_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_range)
