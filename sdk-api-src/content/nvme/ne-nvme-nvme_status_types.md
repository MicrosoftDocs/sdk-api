---
UID: NE:nvme.NVME_STATUS_TYPES
tech.root: fs
title: NVME_STATUS_TYPES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values indicating the type of status code that is posted by the controller in a completion queue entry when a command is completed.
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
 - NVME_STATUS_TYPES
f1_keywords:
 - NVME_STATUS_TYPES
 - nvme/NVME_STATUS_TYPES
dev_langs:
 - c++
---

# NVME_STATUS_TYPES enumeration


## -description

Contains values indicating the type of status code that is posted by the controller in a completion queue entry when a command is completed.

## -enum-fields

### -field NVME_STATUS_TYPE_GENERIC_COMMAND

Indicates that the command specified by the Command and Submission Queue identifiers in the completion queue entry has completed. These status values are generic across all command types, and include such conditions as success, opcode not supported, and invalid field.

One of the status codes in the [NVME_STATUS_GENERIC_COMMAND_CODES](ne-nvme-nvme_status_generic_command_codes.md) enumeration.

### -field NVME_STATUS_TYPE_COMMAND_SPECIFIC

Indicates a status value that is specific to a particular command opcode. These values may indicate additional processing is required. Status values such as invalid firmware image or exceeded maximum number of queues is reported with this type.

One of the status codes in the [NVME_STATUS_COMMAND_SPECIFIC_CODES](ne-nvme-nvme_status_command_specific_codes.md) enumeration.

### -field NVME_STATUS_TYPE_MEDIA_ERROR

A status value that indicates a media specific error occurred in the NVM, or a data integrity error.

One of the status codes in the [NVME_STATUS_MEDIA_ERROR_CODES](ne-nvme-nvme_status_media_error_codes.md) enumeration.

### -field NVME_STATUS_TYPE_VENDOR_SPECIFIC

Indicates a vendor specific status code.

## -remarks

When a command is completed, a value from this enumeration is posted by the controller in the **SCT** field of a [NVME_COMMAND_STATUS](ns-nvme-nvme_command_status.md) structure in the **Status** field of a [Completion Queue entry](ns-nvme-nvme_completion_entry.md).

## -see-also

- [Completion Queue entry](ns-nvme-nvme_completion_entry.md)

