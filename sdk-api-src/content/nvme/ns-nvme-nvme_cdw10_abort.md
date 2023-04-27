---
UID: NS:nvme.NVME_CDW10_ABORT
tech.root: fs
title: NVME_CDW10_ABORT
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Abort command that is used to abort a specific command previously submitted to the Admin Submission Queue or an I/O Submission Queue.
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
req.typenames: NVME_CDW10_ABORT, *PNVME_CDW10_ABORT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_ABORT
 - NVME_CDW10_ABORT
f1_keywords:
 - PNVME_CDW10_ABORT
 - nvme/PNVME_CDW10_ABORT
 - NVME_CDW10_ABORT
 - nvme/NVME_CDW10_ABORT
dev_langs:
 - c++
---

# NVME_CDW10_ABORT structure


## -description

Contains parameters for the Abort command that is used to abort a specific command previously submitted to the Admin Submission Queue or an I/O Submission Queue.

The **NVME_CDW10_ABORT** structure is used in the **CDW10** field of the **ABORT** parameter in the [Command](ns-nvme-nvme_command.md) structure. All other command specific fields in the **ABORT** structure are reserved.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.SQID

The Submission Queue Identifier (SQID) field specifies the identifier of the Submission Queue associated with the command to be aborted.

### -field DUMMYSTRUCTNAME.CID

The Command Identifier (CID) field specifies the command identifier of the command to be aborted, that was specified in the **CID** field of the [NVME_COMMAND_DWORD0](ns-nvme-nvme_command_dword0.md) structure within the **CDW0** field of the [Command](ns-nvme-nvme_command.md) itself.

### -field AsUlong

## -remarks

Host software may have multiple Abort commands outstanding, subject to the constraints of the Abort Command Limit indicated in the **ACL** field of the [Identify Controller data structure](ns-nvme-nvme_identify_controller_data.md).

An Abort command is a best effort command; the command to abort may have already completed, currently be in execution, or may be deeply queued. If or when a controller chooses to complete the command when the command to abort is not found, is implementation specific.

## -see-also

- [NVME_COMMAND_DWORD0](ns-nvme-nvme_command_dword0.md) structure
- [Command](ns-nvme-nvme_command.md)

