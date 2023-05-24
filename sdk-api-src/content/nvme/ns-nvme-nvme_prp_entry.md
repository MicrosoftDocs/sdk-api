---
UID: NS:nvme.NVME_PRP_ENTRY
tech.root: fs
title: NVME_PRP_ENTRY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the Page Base Address and Offset (PBAO) of a pointer to a physical memory page.
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
req.typenames: NVME_PRP_ENTRY, *PNVME_PRP_ENTRY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_PRP_ENTRY
 - NVME_PRP_ENTRY
f1_keywords:
 - PNVME_PRP_ENTRY
 - nvme/PNVME_PRP_ENTRY
 - NVME_PRP_ENTRY
 - nvme/NVME_PRP_ENTRY
dev_langs:
 - c++
---

# NVME_PRP_ENTRY structure


## -description

Contains fields that specify the Page Base Address and Offset (PBAO) of a pointer to a physical memory page.

A Physical Region Page (PRP) Entry is a pointer to a physical memory page. PRPs are used as a scatter/gather mechanism for data transfers between the controller and memory. To enable efficient out of order data transfers between the controller and the host, PRP entries are a fixed size.

The size of the physical memory page is configured by host software in the **MPS** field of the [Controller Configuration](ns-nvme-nvme_controller_configuration.md) structure, and the size of the Offset field is determined by the **MPS** value.

This structure is used in the **PRP1** and **PRP2** fields of the [NVME_COMMAND](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.Reserved0

A reserved field.

### -field DUMMYSTRUCTNAME.PBAO

Indicates the 64-bit physical memory page address.

The lower bits (n:2) of this field indicate the offset within the memory page. If the memory page size is 4KB, then bits 02:11 form the Offset; if the memory page size is 8KB, then bits 02:12 form the Offset, and so on.

If this entry is not the first PRP entry in the command or a PRP List pointer in a command, then the Offset portion of this field should be cleared to `0h`.

### -field AsUlonglong

## -remarks

## -see-also

