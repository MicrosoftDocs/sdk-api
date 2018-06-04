---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _STORAGE_PROTOCOL_COMMAND structure


## -description


This structure is used as an input buffer when using the pass-through mechanism to issue  a vendor-specific command to a storage device (via <a href="https://msdn.microsoft.com/library/windows/hardware/dn932068">IOCTL_STORAGE_PROTOCOL_COMMAND</a>).


## -struct-fields




### -field Version

The version of this structure. This should be set to <b>STORAGE_PROTOCOL_STRUCTURE_VERSION</b>.


### -field Length

The size of this structure. This should be set to sizeof(<b>STORAGE_PROTOCOL_COMMAND</b>).


### -field ProtocolType

The protocol type, of type <a href="https://msdn.microsoft.com/library/windows/hardware/dn931818">STORAGE_PROTOCOL_TYPE</a>.


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

 




#### - Command[ANYSIZE_ARRAY]

The vendor-specific command that is to be passed-through to the device. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn932068">IOCTL_STORAGE_PROTOCOL_COMMAND</a>
 

 

