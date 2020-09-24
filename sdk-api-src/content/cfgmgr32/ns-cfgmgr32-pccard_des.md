---
UID: NS:cfgmgr32.PcCard_Des_s
title: PCCARD_DES (cfgmgr32.h)
description: The PCCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PPCCARD_DES","PCCARD_DES","PCCARD_DES structure [Device and Driver Installation]","PPCCARD_DES","PPCCARD_DES structure pointer [Device and Driver Installation]","cfgmgr32/PCCARD_DES","cfgmgr32/PPCCARD_DES","cfgmgrst_c82ff49b-4ae5-478d-a981-26d75408b157.xml","devinst.pccard_des"]
old-location: devinst\pccard_des.htm
tech.root: devinst
ms.assetid: d1bf4d50-70e1-4eff-8973-0b83a31f55fc
ms.date: 12/05/2018
ms.keywords: '*PPCCARD_DES, PCCARD_DES, PCCARD_DES structure [Device and Driver Installation], PPCCARD_DES, PPCCARD_DES structure pointer [Device and Driver Installation], cfgmgr32/PCCARD_DES, cfgmgr32/PPCCARD_DES, cfgmgrst_c82ff49b-4ae5-478d-a981-26d75408b157.xml, devinst.pccard_des'
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
req.typenames: PCCARD_DES, *PPCCARD_DES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PcCard_Des_s
 - cfgmgr32/PcCard_Des_s
 - PPCCARD_DES
 - cfgmgr32/PPCCARD_DES
 - PCCARD_DES
 - cfgmgr32/PCCARD_DES
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
 - PCCARD_DES
---

# PCCARD_DES structure


## -description

The PCCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field PCD_Count

Must be 1.

### -field PCD_Type

<i>Not used.</i>

### -field PCD_Flags

One bit flag from <i>each</i> of the flag sets described in the following table.

<table>
<tr>
<th></th>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td colspan="2">
<i>I/O Addressing Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
fPCD_IO_8

</td>
<td>
The device uses 8-bit I/O addressing.

</td>
</tr>
<tr>
<td></td>
<td>
fPCD_IO_16

</td>
<td>
The device uses 16-bit I/O addressing.

</td>
</tr>
<tr>
<td></td>
<td>
mPCD_IO_8_16

</td>
<td>
Bitmask for the bit within <b>PCD_Flags</b> that specifies 8-bit or 16-bit I/O addressing.

</td>
</tr>
<tr>
<td colspan="2">
<i>Memory Addressing Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
fPCD_MEM_8

</td>
<td>
The device uses 8-bit memory addressing.

</td>
</tr>
<tr>
<td></td>
<td>
fPCD_MEM_16

</td>
<td>
The device uses 16-bit memory addressing.

</td>
</tr>
<tr>
<td></td>
<td>
mPCD_MEM_8_16

</td>
<td>
Bitmask for the bit within <b>PCD_Flags</b> that specifies 8-bit or 16-bit memory addressing.

</td>
</tr>
</table>

### -field PCD_ConfigIndex

The 8-bit index value used to locate the device's configuration.

### -field PCD_Reserved

<i>Not used.</i>

### -field PCD_MemoryCardBase1

<i>Optional</i>, card base address of the first memory window.

### -field PCD_MemoryCardBase2

<i>Optional</i>, card base address of the second memory window.

### -field PCD_MemoryCardBase

This member is currently unused.

### -field PCD_MemoryFlags

This member is currently unused.

### -field PCD_IoFlags

This member is currently unused.

## -see-also

[PCCARD_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-pccard_resource)