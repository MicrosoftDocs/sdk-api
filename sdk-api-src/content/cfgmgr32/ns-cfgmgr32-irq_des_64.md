---
UID: NS:cfgmgr32.IRQ_Des_64_s
title: IRQ_DES_64 (cfgmgr32.h)
description: The IRQ_DES structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. (64 bit)
helpviewer_keywords: ["*PIRQ_DES_64","IRQ_DES","IRQ_DES structure [Device and Driver Installation]","IRQ_DES_64","PIRQ_DES","PIRQ_DES structure pointer [Device and Driver Installation]","cfgmgr32/IRQ_DES","cfgmgr32/PIRQ_DES","cfgmgrst_039f414c-eefc-46f0-acbe-a94d09406d92.xml","devinst.irq_des"]
old-location: devinst\irq_des.htm
tech.root: devinst
ms.assetid: fa8b8d96-6642-4f5a-b65c-0c7470340251
ms.date: 12/05/2018
ms.keywords: '*PIRQ_DES_64, IRQ_DES, IRQ_DES structure [Device and Driver Installation], IRQ_DES_64, PIRQ_DES, PIRQ_DES structure pointer [Device and Driver Installation], cfgmgr32/IRQ_DES, cfgmgr32/PIRQ_DES, cfgmgrst_039f414c-eefc-46f0-acbe-a94d09406d92.xml, devinst.irq_des'
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
req.typenames: IRQ_DES_64, *PIRQ_DES_64
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRQ_Des_64_s
 - cfgmgr32/IRQ_Des_64_s
 - PIRQ_DES_64
 - cfgmgr32/PIRQ_DES_64
 - IRQ_DES_64
 - cfgmgr32/IRQ_DES_64
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
 - IRQ_DES
---

# IRQ_DES_64 structure


## -description

The IRQ_DES structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field IRQD_Count

#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the [IRQ_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_resource_32) structure.

### -field IRQD_Type

Must be set to the constant value <b>IRQType_Range</b>.

### -field IRQD_Group

### -field IRQD_Flags

One bit flag from <i>each</i> of the flag sets described in the following table.

<table>
<tr>
<th></th>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td colspan="2">
<i>Sharing Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fIRQD_Exclusive</b>

</td>
<td>
The IRQ line cannot be shared.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIRQD_Share</b>

</td>
<td>
The IRQ line can be shared.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mIRQD_Share</b>

</td>
<td>
Bitmask for the bits within <b>IRQD_Flags</b> that specify the sharing value.

</td>
</tr>
<tr>
<td colspan="2">
<i>Triggering Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fIRQD_Level</b>

</td>
<td>
The IRQ line is level-triggered.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIRQD_Edge</b>

</td>
<td>
The IRQ line is edge-triggered.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mIRQD_Edge_Level</b>

</td>
<td>
Bitmask for the bits within <b>IRQD_Flags</b> that specify the triggering value.

</td>
</tr>
</table>

### -field IRQD_Alloc_Num

#### For a resource list:

The number of the IRQ line that is allocated to the device.



#### For a resource requirements list:

<i>Not used.</i>

### -field IRQD_Affinity

#### For a resource list:

A bitmask representing the processor affinity of the IRQ line that is allocated to the device. Bit zero represents the first processor, bit two the second, and so on. Set this value to -1 to represent all processors. 



#### For a resource requirements list:

<i>Not used.</i>


##### - IRQD_Affinity.For a resource list:

A bitmask representing the processor affinity of the IRQ line that is allocated to the device. Bit zero represents the first processor, bit two the second, and so on. Set this value to -1 to represent all processors. 


##### - IRQD_Affinity.For a resource requirements list:

<i>Not used.</i>


##### - IRQD_Alloc_Num.For a resource list:

The number of the IRQ line that is allocated to the device.


##### - IRQD_Alloc_Num.For a resource requirements list:

<i>Not used.</i>


##### - IRQD_Count.For a resource list:

Zero.


##### - IRQD_Count.For a resource requirements list:

The number of elements in the [IRQ_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_resource_32) structure.

## -see-also

[IRQ_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_range)



[IRQ_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_resource_32)
