---
UID: NE:nvme.NVME_STATUS_MEDIA_ERROR_CODES
tech.root: fs
title: NVME_STATUS_MEDIA_ERROR_CODES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate an error associated with the NVM media or indicate a data integrity type error.
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
 - NVME_STATUS_MEDIA_ERROR_CODES
f1_keywords:
 - NVME_STATUS_MEDIA_ERROR_CODES
 - nvme/NVME_STATUS_MEDIA_ERROR_CODES
dev_langs:
 - c++
---

# NVME_STATUS_MEDIA_ERROR_CODES enumeration


## -description

Contains values that indicate an error associated with the NVM media or indicate a data integrity type error.

These status codes are of the **NVME_STATUS_TYPE_MEDIA_ERROR** [Status Code Type](ne-nvme-nvme_status_types.md) and are posted by the controller in a [Completion Queue entry](ns-nvme-nvme_completion_entry.md) when a command is completed.

## -enum-fields

### -field NVME_STATUS_NVM_WRITE_FAULT

The write data could not be committed to the media.

### -field NVME_STATUS_NVM_UNRECOVERED_READ_ERROR

The read data could not be recovered from the media.

### -field NVME_STATUS_NVM_END_TO_END_GUARD_CHECK_ERROR

The command was aborted due to an end-to-end guard check failure.

### -field NVME_STATUS_NVM_END_TO_END_APPLICATION_TAG_CHECK_ERROR

The command was aborted due to an end-to-end application tag check failure.

### -field NVME_STATUS_NVM_END_TO_END_REFERENCE_TAG_CHECK_ERROR

The command was aborted due to an end-to-end reference tag check failure.

### -field NVME_STATUS_NVM_COMPARE_FAILURE

The command failed due to a miscompare during a Compare command.

### -field NVME_STATUS_NVM_ACCESS_DENIED

Access to the namespace and/or Logical Block Address (LBA) range is denied due to lack of access rights. For more information, see the [TCG Storage Interface Interactions Specification (SIIS)](https://trustedcomputinggroup.org).

### -field NVME_STATUS_NVM_DEALLOCATED_OR_UNWRITTEN_LOGICAL_BLOCK

The command failed due to an attempt to read from an LBA range containing a deallocated or unwritten logical block.

## -remarks

## -see-also

