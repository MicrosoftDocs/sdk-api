---
UID: NI:winioctl.IOCTL_STORAGE_QUERY_PROPERTY
title: IOCTL_STORAGE_QUERY_PROPERTY
description: Windows applications can use this control code to return the properties of a storage device or adapter.
helpviewer_keywords: ["IOCTL_STORAGE_QUERY_PROPERTY","IOCTL_STORAGE_QUERY_PROPERTY control","IOCTL_STORAGE_QUERY_PROPERTY control code [Files]","fs.ioctl_storage_query_property","winioctl/IOCTL_STORAGE_QUERY_PROPERTY"]
old-location: fs\ioctl_storage_query_property.htm
tech.root: fs
ms.assetid: 6755dcd4-e4a0-423f-9dcc-b9719c8e5c88
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_QUERY_PROPERTY, IOCTL_STORAGE_QUERY_PROPERTY control, IOCTL_STORAGE_QUERY_PROPERTY control code [Files], fs.ioctl_storage_query_property, winioctl/IOCTL_STORAGE_QUERY_PROPERTY
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
f1_keywords:
 - IOCTL_STORAGE_QUERY_PROPERTY
 - winioctl/IOCTL_STORAGE_QUERY_PROPERTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_QUERY_PROPERTY
---

# IOCTL_STORAGE_QUERY_PROPERTY IOCTL


## -description

Windows applications can use this control code to return the properties of a storage device or adapter. The request indicates the kind of information to retrieve, such as the inquiry data for a device or the capabilities and limitations of an adapter. **IOCTL_STORAGE_QUERY_PROPERTY** can also be used to determine whether the port driver supports a particular property or which fields in the property descriptor can be modified with a subsequent change-property request.


```cpp
BOOL DeviceIoControl(
     _In_        (HANDLE)       hDevice,                // handle to a partition
     _In_        (DWORD) IOCTL_STORAGE_QUERY_PROPERTY,  // dwIoControlCode
     _In_        (LPVOID)       lpInBuffer,             // input buffer - STORAGE_PROPERTY_QUERY structure
     _In_        (DWORD)        nInBufferSize,          // size of input buffer
     _Out_opt_   (LPVOID)       lpOutBuffer,            // output buffer - see Remarks
     _In_        (DWORD)        nOutBufferSize,         // size of output buffer
     _Out_opt_   (LPDWORD)      lpBytesReturned,        // number of bytes returned
     _Inout_opt_ (LPOVERLAPPED) lpOverlapped            // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

The optional output buffer returned through the *lpOutBuffer* parameter can be one of several structures depending on the value of the **PropertyId** member of the [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) structure pointed to by the *lpInBuffer* parameter. These values are enumerated by the [STORAGE_PROPERTY_ID](ne-winioctl-storage_property_id.md) enumeration. If the **QueryType** member of the **STORAGE_PROPERTY_QUERY** is set to **PropertyExistsQuery** then no structure is returned.

## -see-also

* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [STORAGE_DESCRIPTOR_HEADER](ns-winioctl-storage_descriptor_header.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)