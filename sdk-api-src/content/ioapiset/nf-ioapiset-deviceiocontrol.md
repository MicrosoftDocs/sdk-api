---
UID: NF:ioapiset.DeviceIoControl
title: DeviceIoControl function
author: windows-sdk-content
description: Sends a control code directly to a specified device driver, causing the corresponding device to perform the corresponding operation.
old-location: base\deviceiocontrol.htm
tech.root: devio
ms.assetid: 1d35c087-6672-4fc6-baa1-a886dd9d3878
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: DeviceIoControl, DeviceIoControl function, _win32_deviceiocontrol, base.deviceiocontrol, ioapiset/DeviceIoControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeviceIoControl function


## -description


Sends a control code directly to a specified device driver, causing the corresponding device to 
    perform the corresponding operation.


## -parameters




### -param hDevice [in]

A handle to the device on which the operation is to be performed. The device is typically a volume, 
      directory, file, or stream. To retrieve a device handle, use the 
      <a href="base.createfile">CreateFile</a> function. For more information, see 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_INSUFFICIENT_BUFFER</b>, and <i>lpBytesReturned</i> is zero.

If the output buffer is too small to hold all of the data but can hold some entries, some drivers will return 
       as much data as fits. In this case, the call fails, 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
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
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>. If 
       <i>hDevice</i> is associated with an I/O completion port, you can retrieve the number of 
       bytes returned by calling 
       <a href="base.getqueuedcompletionstatus">GetQueuedCompletionStatus</a>.


### -param lpOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.

If <i>hDevice</i> was opened without specifying 
       <b>FILE_FLAG_OVERLAPPED</b>, <i>lpOverlapped</i> is ignored.

If <i>hDevice</i> was opened with the <b>FILE_FLAG_OVERLAPPED</b> flag, 
       the operation is performed as an overlapped (asynchronous) operation. In this case, 
       <i>lpOverlapped</i> must point to a valid 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an 
       event object. Otherwise, the function fails in unpredictable ways.

For overlapped operations, 
       <b>DeviceIoControl</b> returns immediately, and the event 
       object is signaled when the operation has been completed. Otherwise, the function does not return until the 
       operation has been completed or an error occurs.


## -returns



If the operation completes successfully, the return value is nonzero.

If the operation fails or is pending, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To retrieve a handle to the device, you must call the 
     <a href="base.createfile">CreateFile</a> function with either the name of a device or 
     the name of the driver associated with a device. To specify a device name, use the following format:

\\.\<i>DeviceName</i>

<b>DeviceIoControl</b> can accept a handle to a specific 
     device. For example, to open a handle to the logical drive A: with 
     <a href="base.createfile">CreateFile</a>, specify \\.\a:. Alternatively, you can use the 
     names \\.\PhysicalDrive0, \\.\PhysicalDrive1, and so on, to open handles to the physical drives on a system.

You should specify the <b>FILE_SHARE_READ</b> and 
    <b>FILE_SHARE_WRITE</b> access flags when calling 
    <a href="base.createfile">CreateFile</a> to open a handle to a device driver. However, 
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
<a href="https://msdn.microsoft.com/a9aed6bb-05aa-4378-837a-ea7ccda39ba4">Communications Control Codes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e2e671c7-ef65-4401-8016-649e86f84fec">Directory Management Control Codes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/027fffdb-62a1-47d8-b69f-c2fcf7f9ac97">Power Management Control Codes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
</li>
</ul>

#### Examples

For an example that uses <b>DeviceIoControl</b>, see 
     <a href="https://msdn.microsoft.com/b4dbda89-effb-43f7-b3cc-774db57862a9">Calling DeviceIoControl</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/2dffd86a-162c-4e09-bfa1-73b87522741a">Device Input and Output Control (IOCTL)</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="base.getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

