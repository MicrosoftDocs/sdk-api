---
UID: NF:ioapiset.DeviceIoControl
title: DeviceIoControl function (ioapiset.h)
description: Sends a control code directly to a specified device driver, causing the corresponding device to perform the corresponding operation.
old-location: base\deviceiocontrol.htm
tech.root: devio
ms.assetid: 1d35c087-6672-4fc6-baa1-a886dd9d3878
ms.date: 12/05/2018
ms.keywords: DeviceIoControl, DeviceIoControl function, _win32_deviceiocontrol, base.deviceiocontrol, ioapiset/DeviceIoControl
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeviceIoControl
 - ioapiset/DeviceIoControl
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
---

## -description

Sends a control code directly to a specified device driver, causing the corresponding device to perform the corresponding operation.

See the [Assign drive letter sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io/dledit).

## -parameters

### -param hDevice [in]

A handle to the device on which the operation is to be performed. The device is typically a volume, 
      directory, file, or stream. To retrieve a device handle, use the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. For more information, see 
      Remarks.

### -param dwIoControlCode [in]

The control code for the operation. This value identifies the specific operation to be performed and the 
       type of device on which to perform it.

For a list of the control codes, see Remarks. The documentation for each control code provides usage details 
       for the <i>lpInBuffer</i>, <i>nInBufferSize</i>, 
       <i>lpOutBuffer</i>, and <i>nOutBufferSize</i> parameters.

### -param lpInBuffer [in, optional]

A pointer to the input buffer that contains the data required to perform the operation. The format of this 
       data depends on the value of the <i>dwIoControlCode</i> parameter.

This parameter can be <b>NULL</b> if <i>dwIoControlCode</i> specifies 
       an operation that does not require input data.

### -param nInBufferSize [in]

The size of the input buffer, in bytes.

### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the data returned by the operation. The format of this 
       data depends on the value of the <i>dwIoControlCode</i> parameter.

This parameter can be <b>NULL</b> if <i>dwIoControlCode</i> specifies 
       an operation that does not return data.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes.

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

If the output buffer is too small to receive any data,  the call fails, 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_INSUFFICIENT_BUFFER</b>, and <i>lpBytesReturned</i> is zero.

If the output buffer is too small to hold all of the data but can hold some entries, some drivers will return 
       as much data as fits. In this case, the call fails, 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_MORE_DATA</b>, and <i>lpBytesReturned</i> indicates the amount 
       of data received. Your application should call 
       <b>DeviceIoControl</b> again with the same operation, 
       specifying a new starting point.

If <i>lpOverlapped</i> is <b>NULL</b>, 
       <i>lpBytesReturned</i> cannot be <b>NULL</b>. Even when an operation 
       returns no output data and <i>lpOutBuffer</i> is <b>NULL</b>, 
       <b>DeviceIoControl</b> makes use of 
       <i>lpBytesReturned</i>. After such an operation, the value of 
       <i>lpBytesReturned</i> is meaningless.

If <i>lpOverlapped</i> is not <b>NULL</b>, 
       <i>lpBytesReturned</i> can be <b>NULL</b>. If this parameter is not 
       <b>NULL</b> and the operation returns data, <i>lpBytesReturned</i> is 
       meaningless until the overlapped operation has completed. To retrieve the number of bytes returned, call 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>. If 
       <i>hDevice</i> is associated with an I/O completion port, you can retrieve the number of 
       bytes returned by calling 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>.

### -param lpOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

If <i>hDevice</i> was opened without specifying 
       <b>FILE_FLAG_OVERLAPPED</b>, <i>lpOverlapped</i> is ignored.

If <i>hDevice</i> was opened with the <b>FILE_FLAG_OVERLAPPED</b> flag, 
       the operation is performed as an overlapped (asynchronous) operation. In this case, 
       <i>lpOverlapped</i> must point to a valid 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an 
       event object. Otherwise, the function fails in unpredictable ways.

For overlapped operations, 
       <b>DeviceIoControl</b> returns immediately, and the event 
       object is signaled when the operation has been completed. Otherwise, the function does not return until the 
       operation has been completed or an error occurs.

## -returns

If the operation completes successfully, the return value is nonzero (TRUE).

If the operation fails or is pending, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To retrieve a handle to the device, you must call the 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function with either the name of a device or 
     the name of the driver associated with a device. To specify a device name, use the following format:

\\.&#92;<i>DeviceName</i>

<b>DeviceIoControl</b> can accept a handle to a specific 
     device. For example, to open a handle to the logical drive A: with 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>, specify \\.\a:. Alternatively, you can use the 
     names \\.\PhysicalDrive0, \\.\PhysicalDrive1, and so on, to open handles to the physical drives on a system.

You should specify the <b>FILE_SHARE_READ</b> and 
    <b>FILE_SHARE_WRITE</b> access flags when calling 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to open a handle to a device driver. However, 
    when you open a communications resource, such as a serial port, you must specify exclusive access. Use the other 
    <b>CreateFile</b> parameters as follows when opening a device 
    handle:

<ul>
<li>The <i>fdwCreate</i> parameter must specify 
      <b>OPEN_EXISTING</b>.</li>
<li>The <i>hTemplateFile</i> parameter must be <b>NULL</b>.</li>
<li>The <i>fdwAttrsAndFlags</i> parameter can specify 
      <b>FILE_FLAG_OVERLAPPED</b> to indicate that the returned handle can be used in overlapped 
      (asynchronous) I/O operations.</li>
</ul>
For lists of supported control codes, see the following topics:

<ul>
<li>
<a href="/windows-hardware/drivers/storage/cd-rom-io-control-codes">CD-ROM Control Codes</a>
</li>
<li>
<a href="/windows/desktop/DevIO/communications-control-codes">Communications Control Codes</a>
</li>
<li>
<a href="/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>
</li>
<li>
<a href="/windows/desktop/FileIO/directory-management-control-codes">Directory Management Control Codes</a>
</li>
<li>
<a href="/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>
</li>
<li>
<a href="/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
</li>
<li>
<a href="/windows/desktop/Power/power-management-control-codes">Power Management Control Codes</a>
</li>
<li>
<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
</li>
</ul>

#### Examples

For an example that uses <b>DeviceIoControl</b>, see <a href="/windows/desktop/DevIO/calling-deviceiocontrol">Calling DeviceIoControl</a>.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>

<a href="/windows/desktop/DevIO/device-input-and-output-control-ioctl-">Device Input and Output Control (IOCTL)</a>

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>

[Assign drive letter sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io/dledit)
