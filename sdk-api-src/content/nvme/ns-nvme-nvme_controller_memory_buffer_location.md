---
UID: NS:nvme.NVME_CONTROLLER_MEMORY_BUFFER_LOCATION
tech.root: fs
title: NVME_CONTROLLER_MEMORY_BUFFER_LOCATION
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines the location of the optional Controller Memory Buffer Location register in the **CMBLOC** field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVME_CONTROLLER_MEMORY_BUFFER_LOCATION, *PNVME_CONTROLLER_MEMORY_BUFFER_LOCATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTROLLER_MEMORY_BUFFER_LOCATION
 - NVME_CONTROLLER_MEMORY_BUFFER_LOCATION
f1_keywords:
 - PNVME_CONTROLLER_MEMORY_BUFFER_LOCATION
 - nvme/PNVME_CONTROLLER_MEMORY_BUFFER_LOCATION
 - NVME_CONTROLLER_MEMORY_BUFFER_LOCATION
 - nvme/NVME_CONTROLLER_MEMORY_BUFFER_LOCATION
dev_langs:
 - c++
---

# NVME_CONTROLLER_MEMORY_BUFFER_LOCATION structure


## -description

Defines the location of the optional Controller Memory Buffer Location register in the **CMBLOC** field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.

If the Controller Memory Buffer Size **CMBSZ** field of **NVME_CONTROLLER_REGISTERS** has a value of `0`, this register is reserved.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.BIR

Indicates the Base Address Register (BAR) that contains the Controller Memory Buffer. For a 64-bit BAR, the BAR for the lower 32-bits of the address is specified.

Valid values for this field are: `0h`, `2h`, `3h`, `4h`, and `5h`.

### -field DUMMYSTRUCTNAME.Reserved

### -field DUMMYSTRUCTNAME.OFST

Indicates the offset of the Controller Memory Buffer in multiples of the Size Unit specified in the **CMBSZ** field of the **NVME_CONTROLLER_REGISTERS** structure. This value is 4KB aligned.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md)
- [NVME_CONTROLLER_MEMORY_BUFFER_SIZE](ns-nvme-nvme_controller_memory_buffer_size.md)

