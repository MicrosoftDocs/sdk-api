---
UID: NS:cfgmgr32.IO_Range_s
title: IO_RANGE (cfgmgr32.h)
description: The IO_RANGE structure specifies a resource requirements list that describes I/O port usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PIO_RANGE","IO_RANGE","IO_RANGE structure [Device and Driver Installation]","PIO_RANGE","PIO_RANGE structure pointer [Device and Driver Installation]","cfgmgr32/IO_RANGE","cfgmgr32/PIO_RANGE","cfgmgrst_50f5c8b2-3154-4bda-aee0-3a8aea22ff4a.xml","devinst.io_range"]
old-location: devinst\io_range.htm
tech.root: devinst
ms.assetid: 1793684b-b4c4-4467-9ac9-8c6b1eea65e3
ms.date: 12/05/2018
ms.keywords: '*PIO_RANGE, IO_RANGE, IO_RANGE structure [Device and Driver Installation], PIO_RANGE, PIO_RANGE structure pointer [Device and Driver Installation], cfgmgr32/IO_RANGE, cfgmgr32/PIO_RANGE, cfgmgrst_50f5c8b2-3154-4bda-aee0-3a8aea22ff4a.xml, devinst.io_range'
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
req.typenames: IO_RANGE, *PIO_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IO_Range_s
 - cfgmgr32/IO_Range_s
 - PIO_RANGE
 - cfgmgr32/PIO_RANGE
 - IO_RANGE
 - cfgmgr32/IO_RANGE
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
 - IO_RANGE
---

# IO_RANGE structure


## -description

The IO_RANGE structure specifies a resource requirements list that describes I/O port usage for a device instance. For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field IOR_Align

Mask used to specify the port address boundary on which the first allocated I/O port address must be aligned.

### -field IOR_nPorts

The number of I/O port addresses required by the device.

### -field IOR_Min

The lowest-numbered of a range of contiguous I/O port addresses that can be allocated to the device.

### -field IOR_Max

The highest-numbered of a range of contiguous I/O port addresses that can be allocated to the device.

### -field IOR_RangeFlags

One bit flag from [IO_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_des) structure. For more information, see the following <b>Remarks</b> section.

### -field IOR_Alias

One of the bit flags described in the following table.

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
IO_ALIAS_10_BIT_DECODE

</td>
<td>
The device decodes 10 bits of the port address.

</td>
</tr>
<tr>
<td>
IO_ALIAS_12_BIT_DECODE

</td>
<td>
The device decodes 12 bits of the port address.

</td>
</tr>
<tr>
<td>
IO_ALIAS_16_BIT_DECODE

</td>
<td>
The device decodes 16 bits of the port address.

</td>
</tr>
<tr>
<td>
IO_ALIAS_POSITIVE_DECODE

</td>
<td>
The device uses "positive decode" instead of "subtractive decode."

</td>
</tr>
</table>
 

For more information, see the following <b>Remarks</b> section.

## -remarks

The flags specified for <b>IOR_Alias</b> have the same interpretation as the address decoding flags specified for <b>IOD_DesFlags</b>. (However, the two sets of flags are not equivalent in assigned values and cannot be used interchangeably.) A resource requirements list can be specified using either set of flags, but using decode flags in <b>IOD_DesFlags</b> is recommended. If address decoding flags are specified using <i>both</i><b>IOD_DesFlags</b> and <b>IOR_Alias</b>, contents of the latter overrides the former.

## -see-also

[IO_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_des)