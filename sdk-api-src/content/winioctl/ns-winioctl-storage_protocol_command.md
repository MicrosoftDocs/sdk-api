---
UID: NS:winioctl._STORAGE_PROTOCOL_COMMAND
title: STORAGE_PROTOCOL_COMMAND
description: This structure is used as an input buffer when using the pass-through mechanism to issue a vendor-specific command to a storage device (via IOCTL_STORAGE_PROTOCOL_COMMAND).
helpviewer_keywords: ["*PSTORAGE_PROTOCOL_COMMAND","PSTORAGE_PROTOCOL_COMMAND","PSTORAGE_PROTOCOL_COMMAND structure pointer [Files]","STORAGE_PROTOCOL_COMMAND","STORAGE_PROTOCOL_COMMAND structure [Files]","fs.storage_protocol_command","winioctl/PSTORAGE_PROTOCOL_COMMAND","winioctl/STORAGE_PROTOCOL_COMMAND"]
old-location: fs\storage_protocol_command.htm
tech.root: fs
ms.assetid: A2F61F18-A5DE-41D5-95D6-E341009484FF
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROTOCOL_COMMAND, PSTORAGE_PROTOCOL_COMMAND, PSTORAGE_PROTOCOL_COMMAND structure pointer [Files], STORAGE_PROTOCOL_COMMAND, STORAGE_PROTOCOL_COMMAND structure [Files], fs.storage_protocol_command, winioctl/PSTORAGE_PROTOCOL_COMMAND, winioctl/STORAGE_PROTOCOL_COMMAND'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND
req.redist: 
f1_keywords:
 - _STORAGE_PROTOCOL_COMMAND
 - winioctl/_STORAGE_PROTOCOL_COMMAND
 - PSTORAGE_PROTOCOL_COMMAND
 - winioctl/PSTORAGE_PROTOCOL_COMMAND
 - STORAGE_PROTOCOL_COMMAND
 - winioctl/STORAGE_PROTOCOL_COMMAND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - STORAGE_PROTOCOL_COMMAND
---

# STORAGE_PROTOCOL_COMMAND structure


## -description

This structure is used as an input buffer when using the pass-through mechanism to issue  a vendor-specific command to a storage device (via <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command">IOCTL_STORAGE_PROTOCOL_COMMAND</a>).

## -struct-fields

### -field Version

The version of this structure. This should be set to <b>STORAGE_PROTOCOL_STRUCTURE_VERSION</b>.

### -field Length

The size of this structure. This should be set to sizeof(<b>STORAGE_PROTOCOL_COMMAND</b>).

### -field ProtocolType

The protocol type, of type <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_type">STORAGE_PROTOCOL_TYPE</a>.

### -field Flags

Flags set for this request. The following are valid flags.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST</b></td>
<td>This flag indicates the request to target an adapter instead of device.</td>
</tr>
</table>

### -field ReturnStatus

The status of the request made to the storage device. In Windows 10, possible values include: 

<table>
<tr>
<th>Status value</th>
<th>Description</th>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_PENDING</b></td>
<td>The request is pending.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_SUCCESS</b></td>
<td>The request has completed successfully.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_ERROR</b></td>
<td>The request has encountered an error.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_INVALID_REQUEST</b></td>
<td>The request is not valid.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_NO_DEVICE</b></td>
<td>A device is not available to make a request to.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_BUSY</b></td>
<td>The device is busy acting on the request.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_DATA_OVERRUN</b></td>
<td>The device encountered a data overrun while acting on the request.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_INSUFFICIENT_RESOURCES</b></td>
<td>The device cannot complete the request due to insufficient resources.</td>
</tr>
<tr>
<td><b>STORAGE_PROTOCOL_STATUS_NOT_SUPPORTED</b></td>
<td>The request is not supported.</td>
</tr>
</table>

### -field ErrorCode

The error code for this request. This is optionally set.

### -field CommandLength

The length of the command. A non-zero value must be set by the caller.

### -field ErrorInfoLength

The length of the error buffer. This is optionally set and can be set to 0.

### -field DataToDeviceTransferLength

The size of the buffer that is to be transferred to the device. This is only used with a WRITE request.

### -field DataFromDeviceTransferLength

The size of the buffer this is to be transferred from the device. This is only used with a READ request.

### -field TimeOutValue

How long to wait for the device until timing out. This is set in units of seconds.

### -field ErrorInfoOffset

The offset of the error buffer. This must be pointer-aligned.

### -field DataToDeviceBufferOffset

The offset of the buffer that is to be transferred to the device. This must be pointer-aligned and is only used with a WRITE request.

### -field DataFromDeviceBufferOffset

The offset of the buffer that is to be transferred from the device. This must be pointer-aligned and is only used with a READ request.

### -field CommandSpecific

Command-specific data passed along with the command. This depends on the command from the driver, and is optionally set.

### -field Reserved0

Reserved for future use.

### -field FixedProtocolReturnData

The return data. This is optionally set. Some protocols such as NVMe, may return a small amount of data (DWORD0 from completion queue entry) without the need of a separate device data transfer.

### -field Reserved1

Reserved for future use.

### -field Command

The vendor-specific command that is to be passed-through to the device.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command">IOCTL_STORAGE_PROTOCOL_COMMAND</a>
