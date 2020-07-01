---
UID: NF:ioapiset.DeviceIoControl
title: DeviceIoControl function (ioapiset.h)
description: Sends a control code directly to a specified device driver, causing the corresponding device to perform the corresponding operation.
helpviewer_keywords: ["DeviceIoControl","DeviceIoControl function","_win32_deviceiocontrol","base.deviceiocontrol","ioapiset/DeviceIoControl"]
old-location: base\deviceiocontrol.htm
tech.root: devio
ms.assetid: 1d35c087-6672-4fc6-baa1-a886dd9d3878
ms.date: 12/05/2018
ms.keywords: DeviceIoControl, DeviceIoControl function, _win32_deviceiocontrol, base.deviceiocontrol, ioapiset/DeviceIoControl
f1_keywords:
- ioapiset/DeviceIoControl
dev_langs:
- c++
req.header: ioapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
- DeviceIoControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeviceIoControl function

## -description

Sends a control code directly to a specified device driver, causing the corresponding device to perform the corresponding operation.

## -parameters

### -param hDevice [in]

A handle to the device on which the operation is to be performed. The device is typically a volume, directory, file, or stream. To retrieve a device handle, use the [CreateFile](../fileapi/nf-fileapi-createfilea.md) function. For more information, see Remarks.

### -param dwIoControlCode [in]

The control code for the operation. This value identifies the specific operation to be performed and the type of device on which to perform it.

For a list of the control codes, see Remarks. The documentation for each control code provides usage details for the *lpInBuffer*, *nInBufferSize*, *lpOutBuffer*, and *nOutBufferSize* parameters.

### -param lpInBuffer [in, optional]

A pointer to the input buffer that contains the data required to perform the operation. The format of this data depends on the value of the *dwIoControlCode* parameter.

This parameter can be **NULL** if *dwIoControlCode* specifies an operation that does not require input data.

### -param nInBufferSize [in]

The size of the input buffer, in bytes.

### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the data returned by the operation. The format of this data depends on the value of the *dwIoControlCode* parameter.

This parameter can be **NULL** if *dwIoControlCode* specifies an operation that does not return data.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes.

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

If the output buffer is too small to receive any data,  the call fails, [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.

If the output buffer is too small to hold all of the data but can hold some entries, some drivers will return as much data as fits. In this case, the call fails, [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns **ERROR_MORE_DATA**, and *lpBytesReturned* indicates the amount of data received. Your application should call **DeviceIoControl** again with the same operation, specifying a new starting point.

If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**. Even when an operation returns no output data and *lpOutBuffer* is **NULL**, **DeviceIoControl** makes use of *lpBytesReturned*. After such an operation, the value of *lpBytesReturned* is meaningless.

If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**. If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed. To retrieve the number of bytes returned, call [**GetOverlappedResult**](nf-ioapiset-getoverlappedresult.md). If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](nf-ioapiset-getqueuedcompletionstatus.md).

### -param lpOverlapped [in, out, optional]

A pointer to an [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure.

If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.

If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation. In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure that contains a handle to an event object. Otherwise, the function fails in unpredictable ways.

For overlapped operations, **DeviceIoControl** returns immediately, and the event object is signaled when the operation has been completed. Otherwise, the function does not return until the operation has been completed or an error occurs.

## -returns

If the operation completes successfully, the return value is nonzero.

If the operation fails or is pending, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

To retrieve a handle to the device, you must call the [CreateFile](../fileapi/nf-fileapi-createfilea.md) function with either the name of a device or the name of the driver associated with a device. To specify a device name, use the following format:

\\\\.\\*DeviceName*

**DeviceIoControl** can accept a handle to a specific device. For example, to open a handle to the logical drive A: with [CreateFile](../fileapi/nf-fileapi-createfilea.md), specify \\\\.\\a:. Alternatively, you can use the names \\\\.\\PhysicalDrive0, \\\\.\\PhysicalDrive1, and so on, to open handles to the physical drives on a system.

You should specify the **FILE_SHARE_READ** and **FILE_SHARE_WRITE** access flags when calling [CreateFile](../fileapi/nf-fileapi-createfilea.md) to open a handle to a device driver. However, when you open a communications resource, such as a serial port, you must specify exclusive access. Use the other **CreateFile** parameters as follows when opening a device handle:

- The *fdwCreate* parameter must specify  **OPEN_EXISTING**.
- The *hTemplateFile* parameter must be **NULL**.
- The *fdwAttrsAndFlags* parameter can specify  **FILE_FLAG_OVERLAPPED** to indicate that the returned handle can be used in overlapped  (asynchronous) I/O operations.

For lists of supported control codes, see the following topics:

- [Communications Control Codes](/windows/win32/DevIO/communications-control-codes)

- [Device Management Control Codes](/windows/win32/DevIO/device-management-control-codes)

- [Directory Management Control Codes](/windows/win32/FileIO/directory-management-control-codes)

- [Disk Management Control Codes](/windows/win32/FileIO/disk-management-control-codes)

- [File Management Control Codes](/windows/win32/FileIO/file-management-control-codes)

- [Power Management Control Codes](/windows/win32/Power/power-management-control-codes)

- [Volume Management Control Codes](/windows/win32/FileIO/volume-management-control-codes)

### Examples

For an example that uses **DeviceIoControl**, see [Calling DeviceIoControl](/windows/win32/DevIO/calling-deviceiocontrol).

## -see-also

[CreateEvent](../synchapi/nf-synchapi-createeventa.md), [CreateFile](../fileapi/nf-fileapi-createfilea.md), [Device Input and Output Control (IOCTL)](/windows/win32/DevIO/device-input-and-output-control-ioctl-.md), [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md), [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md), [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
