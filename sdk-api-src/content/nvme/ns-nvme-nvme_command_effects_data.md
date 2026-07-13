---
UID: NS:nvme.NVME_COMMAND_EFFECTS_DATA
tech.root: fs
title: NVME_COMMAND_EFFECTS_DATA
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains information that describes the overall possible effect of an Admin or I/O command, including any optional features of the command.
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
req.typenames: NVME_COMMAND_EFFECTS_DATA, *PNVME_COMMAND_EFFECTS_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMMAND_EFFECTS_DATA
 - NVME_COMMAND_EFFECTS_DATA
f1_keywords:
 - PNVME_COMMAND_EFFECTS_DATA
 - nvme/PNVME_COMMAND_EFFECTS_DATA
 - NVME_COMMAND_EFFECTS_DATA
 - nvme/NVME_COMMAND_EFFECTS_DATA
dev_langs:
 - c++
---

# NVME_COMMAND_EFFECTS_DATA structure


## -description

Contains information that describes the overall possible effect of an Admin or I/O command, including any optional features of the command.

This structure is used in the **ACS** and **IOCS** fields of the [NVME_COMMAND_EFFECTS_LOG](ns-nvme-nvme_command_effects_log.md).

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.CSUPP

Indicates whether the command is supported.

When this value is set to `1`, the command is supported by the controller. When this value is cleared to `0`, the command is not supported by the controller and
all other fields in this structure will be cleared to `0h`.

### -field DUMMYSTRUCTNAME.LBCC

Indicates whether the command can modify logical block content in one or more namespaces.

When this value is set to `1`, the command can modify logical block content in one or more namespaces. When this value is cleared to `0`, the command does not modify logical block content in any namespace. Logical block content changes include a write to a logical block.

### -field DUMMYSTRUCTNAME.NCC

Indicates whether the command can change the capabilities of a single namespace.

When this value is set to `1`, the command can change the capabilities of a single namespace. When this value is cleared to `0`, the command does not modify any namespace capabilities for the specified namespace. Namespace capability changes include a logical format change.

### -field DUMMYSTRUCTNAME.NIC

Indicates whether the command can change the number of namespaces or capabilities for multiple namespaces.

When this value is set to `1`, the command can change the number of namespaces or capabilities for multiple namespaces. When this value is cleared to `0`, the command does not modify the number of namespaces or capabilities for multiple namespaces. Namespace inventory changes (NIC) include adding or removing namespaces.

### -field DUMMYSTRUCTNAME.CCC

Indicates whether the command can change controller capabilities.

When this value is set to `1`, the command can change controller capabilities. When this value is cleared to `0`, the command does not modify controller capabilities. Controller capability changes (CCC) include a firmware update that changes the capabilities reported in the CAP register.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.CSE

An [NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS](ne-nvme-nvme_command_effect_sbumission_execution_limits.md) value that defines the command submission and execution recommendations for the associated command.

### -field DUMMYSTRUCTNAME.Reserved1

### -field AsUlong

## -remarks

Host software may take command effects into account when determining how to submit commands and actions to take after the command is complete. If a command changes a particular capability. the host software should re-enumerate and/or re-initialize the associated capability after the command is complete.

For example, if a namespace capability change may occur, then the host software should pause the use of the associated namespace, submit the command that may cause a namespace capability change and wait for its completion, and then re-issue the Identify command.

## -see-also

- [NVME_COMMAND_EFFECTS_LOG](ns-nvme-nvme_command_effects_log.md)

