---
UID: NE:nvme.NVME_NVM_COMMANDS
tech.root: fs
title: NVME_NVM_COMMANDS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a command in the NVM Command Set.
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
 - NVME_NVM_COMMANDS
f1_keywords:
 - NVME_NVM_COMMANDS
 - nvme/NVME_NVM_COMMANDS
dev_langs:
 - c++
---

# NVME_NVM_COMMANDS enumeration


## -description

Contains values that indicate a command in the NVM Command Set.

## -enum-fields

### -field NVME_NVM_COMMAND_FLUSH

The Flush command that commits data and metadata associated with the specified namespace(s) to nonvolatile media. The flush applies to all commands completed prior to the submission of the Flush command. The controller may also flush additional data and/or metadata from any namespace.

### -field NVME_NVM_COMMAND_WRITE

The Write command that writes data and metadata, if applicable, to the NVM controller for the specified logical blocks. The host may also specify protection information to include as part of the operation.

The command uses Command Dword 10, Command Dword 11, Command Dword 12, Command Dword 13, Command Dword 14, and Command Dword 15 fields. If the command uses PRPs for the data transfer, then the Metadata Pointer, PRP Entry 1, and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the Metadata SGL Segment Pointer and SGL Entry 1 fields are used.

### -field NVME_NVM_COMMAND_READ

The Read command that reads data and metadata, if applicable, from the NVM controller for the specified logical blocks. The command may specify protection information to be checked as part of the read operation.

The command uses Command Dword 10, Command Dword 11, Command Dword 12, Command Dword 13, Command Dword 14, and Command Dword 15 fields. If the command uses PRPs for the data transfer, then the Metadata Pointer, PRP Entry 1, and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the Metadata SGL Segment Pointer and SGL Entry 1 fields are used.

### -field NVME_NVM_COMMAND_WRITE_UNCORRECTABLE

The Write Uncorrectable command that is used to mark a range of logical blocks as invalid. When the specified logical block(s) are read after this operation, a failure is returned with [Unrecovered Read Error status](ne-nvme-nvme_status_media_error_codes.md). To clear the invalid logical block status, a write operation is performed on those logical blocks.

The fields used are Command Dword 10, Command Dword 11, and Command Dword 12 fields. All other command specific fields are reserved.

### -field NVME_NVM_COMMAND_COMPARE

The Compare command that reads the logical blocks specified by the command from the medium and compares the data read to a comparison data buffer transferred as part of the command. If the data read from the controller and the comparison data buffer are equivalent with no miscompares, then the command completes successfully. If there is any miscompare, the command completes with an error of Compare Failure. If metadata is provided, then a comparison is also performed for the metadata.

The command uses Command Dword 10, Command Dword 11, Command Dword 12, Command Dword 14, and Command Dword 15 fields. If the command uses PRPs for the data transfer, then the Metadata Pointer, PRP Entry 1, and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the Metadata SGL Segment Pointer and SGL Entry 1 fields are used. All other command specific fields are reserved.

### -field NVME_NVM_COMMAND_WRITE_ZEROES

The Write Zeroes command that is used to set a range of logical blocks to zero. After successful completion of this command, the value returned by subsequent reads of logical blocks in this range shall be zeroes until a write occurs to this LBA range. The metadata for this command shall be all zeroes and the protection information is updated based on CDW12.PRINFO.

The fields used are Command Dword 10, Command Dword 11, Command Dword 12, Command Dword 14, and Command Dword 15 fields.

### -field NVME_NVM_COMMAND_DATASET_MANAGEMENT

The Dataset Management command that is used by the host to indicate attributes for ranges of logical blocks.

This includes attributes like frequency that data is read or written, access size, and other information that may be used to optimize performance and reliability. This command is advisory; a compliant controller may choose to take no action based on information provided.

The command uses Command Dword 10, and Command Dword 11 fields. If the command uses PRPs for the data transfer, then the PRP Entry 1 and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the SGL Entry 1 field is used. All other command specific fields are reserved.

### -field NVME_NVM_COMMAND_RESERVATION_REGISTER

The Reservation Register command that is used to register, unregister, or replace a reservation key.

The command uses Command Dword 10 and a Reservation Register data structure in memory. If the command uses PRPs for the data transfer, then PRP Entry 1 and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the SGL Entry 1 field is used. All other command specific fields are reserved.

### -field NVME_NVM_COMMAND_RESERVATION_REPORT

The Reservation Report command that returns a Reservation Status data structure to memory that describes the registration and reservation status of a namespace.

The size of the Reservation Status data structure is a function of the number of controllers in the NVM Subsystem that are associated with hosts that are registrants of the namespace (for example, there is a Registered Controller data structure for each such controller).

### -field NVME_NVM_COMMAND_RESERVATION_ACQUIRE

The Reservation Acquire command that is used to acquire a reservation on a namespace, preempt a reservation held on a namespace, and abort a reservation held on a namespace.

The command uses Command Dword 10 and a Reservation Acquire data structure in memory. If the command uses PRPs for the data transfer, then PRP Entry 1 and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the SGL Entry 1 field is used. All other command specific fields are reserved.

### -field NVME_NVM_COMMAND_RESERVATION_RELEASE

The Reservation Release command that is used to release or clear a reservation held on a namespace.

The command uses Command Dword 10 and a Reservation Release data structure in memory. If the command uses PRPs for the data transfer, then PRP Entry 1 and PRP Entry 2 fields are used. If the command uses SGLs for the data transfer, then the SGL Entry 1 field is used. All other command specific fields are reserved.

## -remarks

NVM Commands are submitted by the host when the controller is ready as indicated in the [Controller Status](ns-nvme-nvme_controller_status.md) register and after the appropriate I/O Submission Queue(s) and I/O Completion Queue(s) have been created.

## -see-also

