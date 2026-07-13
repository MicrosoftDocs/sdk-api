---
UID: NS:nvme.NVME_ERROR_INFO_LOG
tech.root: fs
title: NVME_ERROR_INFO_LOG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information in an Error Information log page.
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
req.typenames: NVME_ERROR_INFO_LOG, *PNVME_ERROR_INFO_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_ERROR_INFO_LOG
 - NVME_ERROR_INFO_LOG
f1_keywords:
 - PNVME_ERROR_INFO_LOG
 - nvme/PNVME_ERROR_INFO_LOG
 - NVME_ERROR_INFO_LOG
 - nvme/NVME_ERROR_INFO_LOG
dev_langs:
 - c++
---

# NVME_ERROR_INFO_LOG structure


## -description

Contains fields that specify the information in an Error Information log page.

The Error Information log page contains extended error information for a command that completed with an error or reported an error that is not specific to a particular command. Extended error information is provided when [More (**M**)](ns-nvme-nvme_command_status.md) is set to `1` in the **Status** field for the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) associated with the command that completed with an error, or as part of an asynchronous event with an Error status type.

The Error Information log page is global to the controller. This error log may return the last *n* errors. If host software specifies a data transfer of the size of *n* error logs, then the error logs for the last *n* errors is returned. The ordering of the entries is based on the time when the error occurred, with the most recent error being returned as the first log.

The Error Information log page is a set of 64 byte entries; the number of supported entries is indicated in the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure.

This structure is returned by the Get Log Page command. For more information, see [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md).

## -struct-fields

### -field ErrorCount

A 64-bit, incrementing error count, that indicates a unique identifier for this error.

The error count starts at `1h`, is incremented for each unique error log entry, and is retained across power off conditions. A value of `0h` indicates an invalid entry; this value may be used when there are lost entries or when there are fewer errors than the maximum number of entries the controller supports.

### -field SQID

Indicates the Submission Queue Identifier (SQID) of the command that the error information is associated with. If the error is not specific to a particular command then this field is set to `FFFFh`.

### -field CMDID

Indicates the Command Identifier (CMDID) of the command that the error is associated with. If the error is not specific to a particular command then this is set to `FFFFh`.

### -field Status

Indicates the Status Field for the command that completed. 

The Status Field is located in bits 01:15. Bit 0 corresponds to the [Phase Tag (**P**)](ns-nvme-nvme_command_status.md) posted for the command. If the error is not specific to a particular command then this field reports the most applicable status value.

### -field ParameterErrorLocation

A **ParameterErrorLocation** structure containing fields that indicate the Byte and Bit of the command parameter that the error is associated with, if applicable.

If the parameter spans multiple bytes or bits, the location indicates the first byte and bit of the parameter. If the error is not specific to a particular command, this field is set to `FFFFh`.

### -field ParameterErrorLocation.Byte

Indicates the Byte in the command that contained the error.

This value is contained in bits 0:7 of the **ParameterErrorLocation** structure. Valid values are 0 to 63.

### -field ParameterErrorLocation.Bit

Indicates the Bit in the command that contained the error.

This value is contained in bits 8:10 of the **ParameterErrorLocation** structure. Valid values are 0 to 7.

### -field ParameterErrorLocation.Reserved

Bits 11:15 of the **ParameterErrorLocation** structure are reserved.

### -field Lba

Indicates the first Logical Block Address (LBA) that experienced the error condition, if applicable.

### -field NameSpace

Indicates the namespace that the error is associated with, if applicable.

### -field VendorInfoAvailable

When there is additional vendor specific error information available, this field provides the log page identifier associated with that page.

A value of `00h` indicates that no additional information is available. Valid values are in the range of `80h` to `FFh`.

### -field Reserved0

A reserved field.

### -field CommandSpecificInfo

Contains command specific information. If used, the command definition specifies the information returned.

### -field Reserved1

A reserved field.

## -remarks

## -see-also

