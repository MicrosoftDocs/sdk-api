---
UID: NS:cfgmgr32.IRQ_Range_s
title: IRQ_RANGE (cfgmgr32.h)
description: The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PIRQ_RANGE","IRQ_RANGE","IRQ_RANGE structure [Device and Driver Installation]","PIRQ_RANGE","PIRQ_RANGE structure pointer [Device and Driver Installation]","cfgmgr32/IRQ_RANGE","cfgmgr32/PIRQ_RANGE","cfgmgrst_6ee86ca7-d07d-4f1b-9c94-96766a5fd4cb.xml","devinst.irq_range"]
old-location: devinst\irq_range.htm
tech.root: devinst
ms.assetid: 973834cc-0798-414f-a937-5ab14c214559
ms.date: 12/05/2018
ms.keywords: '*PIRQ_RANGE, IRQ_RANGE, IRQ_RANGE structure [Device and Driver Installation], PIRQ_RANGE, PIRQ_RANGE structure pointer [Device and Driver Installation], cfgmgr32/IRQ_RANGE, cfgmgr32/PIRQ_RANGE, cfgmgrst_6ee86ca7-d07d-4f1b-9c94-96766a5fd4cb.xml, devinst.irq_range'
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
req.typenames: IRQ_RANGE, *PIRQ_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRQ_Range_s
 - cfgmgr32/IRQ_Range_s
 - PIRQ_RANGE
 - cfgmgr32/PIRQ_RANGE
 - IRQ_RANGE
 - cfgmgr32/IRQ_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - IRQ_RANGE
---

# IRQ_RANGE structure


## -description

The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance. For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field IRQR_Min

The lowest-numbered of a range of contiguous IRQ lines that can be allocated to the device.

### -field IRQR_Max

The highest-numbered of a range of contiguous IRQ lines that can be allocated to the device.

### -field IRQR_Rsvdz

### -field IRQR_Flags

One bit flag from [IRQ_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_des_32) structure.

## -see-also

[IRQ_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_des_32)