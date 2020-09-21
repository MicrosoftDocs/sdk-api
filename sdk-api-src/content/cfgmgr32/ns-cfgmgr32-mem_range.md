---
UID: NS:cfgmgr32.Mem_Range_s
title: MEM_RANGE (cfgmgr32.h)
description: The MEM_RANGE structure specifies a resource requirements list that describes memory usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PMEM_RANGE","MEM_RANGE","MEM_RANGE structure [Device and Driver Installation]","PMEM_RANGE","PMEM_RANGE structure pointer [Device and Driver Installation]","cfgmgr32/MEM_RANGE","cfgmgr32/PMEM_RANGE","cfgmgrst_f2ac1f4b-c29b-41fd-bacb-e7a8f4bc6f45.xml","devinst.mem_range"]
old-location: devinst\mem_range.htm
tech.root: devinst
ms.assetid: a31ae199-8f4a-4d1f-891c-f1dc11a4edde
ms.date: 12/05/2018
ms.keywords: '*PMEM_RANGE, MEM_RANGE, MEM_RANGE structure [Device and Driver Installation], PMEM_RANGE, PMEM_RANGE structure pointer [Device and Driver Installation], cfgmgr32/MEM_RANGE, cfgmgr32/PMEM_RANGE, cfgmgrst_f2ac1f4b-c29b-41fd-bacb-e7a8f4bc6f45.xml, devinst.mem_range'
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
req.typenames: MEM_RANGE, *PMEM_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Mem_Range_s
 - cfgmgr32/Mem_Range_s
 - PMEM_RANGE
 - cfgmgr32/PMEM_RANGE
 - MEM_RANGE
 - cfgmgr32/MEM_RANGE
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
 - MEM_RANGE
---

# MEM_RANGE structure


## -description

The MEM_RANGE structure specifies a resource requirements list that describes memory usage for a device instance. For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field MR_Align

Mask used to specify the memory address boundary on which the first allocated memory address must be aligned.

### -field MR_nBytes

The number of bytes of memory required by the device.

### -field MR_Min

The lowest-numbered of a range of contiguous memory addresses that can be allocated to the device.

### -field MR_Max

The highest-numbered of a range of contiguous memory addresses that can be allocated to the device.

### -field MR_Flags

One bit flag from [MEM_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_des) structure.

### -field MR_Reserved

<i>For internal use only.</i>

## -see-also

[MEM_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_des)