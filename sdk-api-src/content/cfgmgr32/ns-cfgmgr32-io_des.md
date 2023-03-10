---
UID: NS:cfgmgr32.IO_Des_s
title: IO_DES (cfgmgr32.h)
description: The IO_DES structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PIO_DES","IO_DES","IO_DES structure [Device and Driver Installation]","PIO_DES","PIO_DES structure pointer [Device and Driver Installation]","cfgmgr32/IO_DES","cfgmgr32/PIO_DES","cfgmgrst_027e9190-0074-48e2-89cd-aa86e8a08165.xml","devinst.io_des"]
old-location: devinst\io_des.htm
tech.root: devinst
ms.assetid: 4b2ae544-0254-4221-80df-e2df4a23d15f
ms.date: 12/05/2018
ms.keywords: '*PIO_DES, IO_DES, IO_DES structure [Device and Driver Installation], PIO_DES, PIO_DES structure pointer [Device and Driver Installation], cfgmgr32/IO_DES, cfgmgr32/PIO_DES, cfgmgrst_027e9190-0074-48e2-89cd-aa86e8a08165.xml, devinst.io_des'
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
req.typenames: IO_DES, *PIO_DES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IO_Des_s
 - cfgmgr32/IO_Des_s
 - PIO_DES
 - cfgmgr32/PIO_DES
 - IO_DES
 - cfgmgr32/IO_DES
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
 - IO_DES
---

# IO_DES structure


## -description

The IO_DES structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field IOD_Count

#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the [IO_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_range) array that is included in the [IO_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_resource) structure.

### -field IOD_Type

Must be set to the constant value <b>IOType_Range</b>.

### -field IOD_Alloc_Base

#### For a resource list:

The lowest-numbered of a range of contiguous I/O port addresses allocated to the device.



#### For a resource requirements list:

Zero.

### -field IOD_Alloc_End

#### For a resource list:

The highest-numbered of a range of contiguous I/O port addresses allocated to the device.



#### For a resource requirements list:

Zero.

### -field IOD_DesFlags

One bit flag from <i>each</i> of the flag sets described in the following table.

<table>
<tr>
<th></th>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td colspan="2">
<i>Port Type Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_IO</b>

</td>
<td>
The device is accessed in I/O address space.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_Memory</b>

</td>
<td>
The device is accessed in memory address space.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_PortType</b>

</td>
<td>
Bitmask for the bits within <b>IOD_DesFlags</b> that specify the port type value.

</td>
</tr>
<tr>
<td colspan="2">
<i>Decode Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_10_BIT_DECODE</b>

</td>
<td>
The device decodes 10 bits of the port address.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_12_BIT_DECODE</b>

</td>
<td>
The device decodes 12 bits of the port address.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_16_BIT_DECODE</b>

</td>
<td>
The device decodes 16 bits of the port address.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_POSITIVE_DECODE</b>

</td>
<td>
The device uses "positive decode" instead of "subtractive decode."

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_DECODE</b>

</td>
<td>
Bitmask for the bits within <b>IOD_DesFlags</b> that specify the decode value.

</td>
</tr>
</table>

## -see-also

[IO_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_range)



[IO_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_resource)