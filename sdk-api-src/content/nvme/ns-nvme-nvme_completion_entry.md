---
UID: NS:nvme.NVME_COMPLETION_ENTRY
tech.root: fs
title: NVME_COMPLETION_ENTRY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Specifies an entry in the Completion Queue that is 16 bytes in size.
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
req.typenames: NVME_COMPLETION_ENTRY, *PNVME_COMPLETION_ENTRY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMPLETION_ENTRY
 - NVME_COMPLETION_ENTRY
f1_keywords:
 - PNVME_COMPLETION_ENTRY
 - nvme/PNVME_COMPLETION_ENTRY
 - NVME_COMPLETION_ENTRY
 - nvme/NVME_COMPLETION_ENTRY
dev_langs:
 - c++
---

# NVME_COMPLETION_ENTRY structure


## -description

Specifies an entry in the Completion Queue that is 16 bytes in size.

## -struct-fields

### -field DW0

The contents of Dword 0 contain command specific information.

If a command uses Dword 0, then the definition of this Dword is contained within the associated command definition. If a command does not use Dword 0, then this field is reserved.

### -field Reserved

The contents of Dword 1 which are reserved.

### -field DW2

A union that contains the information in Dword 2.

### -field DW2.DUMMYSTRUCTNAME

### -field DW2.DUMMYSTRUCTNAME.SQHD

Indicates the current Submission Queue Head pointer for the Submission Queue indicated in the SQ Identifier (**SQID**) field. This is used to indicate to the host the Submission Queue entries that have been consumed and may be re-used for new entries.

> [!NOTE]
> The value returned is the value of the Submission Queue Head pointer when the completion queue entry was created. By the time host software consumes the completion queue entry, the controller may have an SQ Head pointer that has advanced beyond the value indicated.

### -field DW2.DUMMYSTRUCTNAME.SQID

Specifies the Submission Queue to which the associated command was issued to. The **SQID** field is used in combination with the Command Identifier (**CID**) by the host software to uniquely determine the completed command when more than one Submission Queue shares a single Completion Queue.

### -field DW2.AsUlong

### -field DW3

A union that contains the information in Dword 3.

### -field DW3.DUMMYSTRUCTNAME

### -field DW3.DUMMYSTRUCTNAME.CID

Indicates the identifier of the command that is being completed.

This identifier is assigned by host software when the command is submitted to the Submission Queue. The combination of the SQ Identifier **SQID** and Command Identifier **CID** uniquely identifies the command that is being completed. The maximum number of requests outstanding at one time is 64K.

### -field DW3.DUMMYSTRUCTNAME.Status

A [NVME_COMMAND_STATUS](ns-nvme-nvme_command_status.md) structure that indicates the status for the command that is being completed.

A value of `0h` for this Field indicates a successful command completion with no fatal or non-fatal error conditions. Unless otherwise noted, if a command fails to complete successfully for multiple reasons, then the particular status code returned is chosen by the vendor.

### -field DW3.AsUlong

## -remarks

## -see-also

