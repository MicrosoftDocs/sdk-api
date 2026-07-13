---
UID: NS:nvme.NVME_COMMAND_DWORD0
tech.root: fs
title: NVME_COMMAND_DWORD0
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters that are common for all Admin commands and NVM commands.
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
req.typenames: NVME_COMMAND_DWORD0, *PNVME_COMMAND_DWORD0
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMMAND_DWORD0
 - NVME_COMMAND_DWORD0
f1_keywords:
 - PNVME_COMMAND_DWORD0
 - nvme/PNVME_COMMAND_DWORD0
 - NVME_COMMAND_DWORD0
 - nvme/NVME_COMMAND_DWORD0
dev_langs:
 - c++
---

# NVME_COMMAND_DWORD0 structure


## -description

Contains parameters that are common for all Admin commands and NVM commands.

This structure is used in the **CDW0** field of the [NVME_COMMAND](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.OPC

Specifies the Opcode (OPC) of the command to be executed.

### -field DUMMYSTRUCTNAME.FUSE

An [NVME_FUSED_OPERATION_CODES](ne-nvme-nvme_fused_operation_codes.md) value that specifies whether this command is part of a fused operation and if so, which command it is in the sequence.

In a fused operation, a complex command is created by *fusing* together two simpler commands.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.PSDT

Specifies whether Physical Region Pages (PRPs) or Scatter Gather Lists (SGLs) are used for any data transfer associated with the command. PRPs are used for all Admin commands.

This field uses the following values:

| Value | Definition                       |
|-------|----------------------------------|
| 00b   | PRPs are used for this transfer. |
| 01b   | SGLs are used for this transfer. |
| 10b   | SGLs are used for this transfer. |
| 11b   | Reserved                         |

If there is metadata that is not interleaved with the logical block data, as specified in the [Format NVM command](ns-nvme-nvme_command.md#-field-u.formatnvm), then the Metadata Pointer (**MPTR**) field in the [NVME_COMMAND](ns-nvme-nvme_command.md) structure is used to point to the metadata. The definition of the **MPTR** field is dependent on the setting in this field.

### -field DUMMYSTRUCTNAME.CID

Specifies a unique identifier for the command when combined with the Submission Queue identifier (**SQID**) in the [command completion entry](ns-nvme-nvme_completion_entry.md).

### -field AsUlong

## -remarks

## -see-also

