---
UID: NE:nvme.NVME_FUSED_OPERATION_CODES
tech.root: fs
title: NVME_FUSED_OPERATION_CODES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate whether a command is the first or second command in a fused operation.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_FUSED_OPERATION_CODES
f1_keywords:
 - NVME_FUSED_OPERATION_CODES
 - nvme/NVME_FUSED_OPERATION_CODES
dev_langs:
 - c++
---

# NVME_FUSED_OPERATION_CODES enumeration


## -description

Contains values that indicate whether a command is the first or second command in a fused operation.

## -enum-fields

### -field NVME_FUSED_OPERATION_NORMAL

A normal operation without fusing commands.

### -field NVME_FUSED_OPERATION_FIRST_CMD

The first command in a fused operation.

### -field NVME_FUSED_OPERATION_SECOND_CMD

The second command in a fused operation.

## -remarks

Use this enumeration to specify values in the **FUSE** field of the [NVME_COMMAND_DWORD0](ns-nvme-nvme_command_dword0.md) structure to indicate whether a command is part of a fused operation.

## -see-also

[NVME_COMMAND_DWORD0](ns-nvme-nvme_command_dword0.md)

