---
UID: NF:winternl.NtDeviceIoControlFile
title: NtDeviceIoControlFile function (winternl.h)
description: Deprecated. Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle. NtDeviceIoControlFile is superseded by DeviceIoControl.
helpviewer_keywords: ["NtDeviceIoControlFile","NtDeviceIoControlFile function [Windows API]","winprog.ntdeviceiocontrolfile","winternl/NtDeviceIoControlFile","winui.ntdeviceiocontrolfile"]
old-location: winprog\ntdeviceiocontrolfile.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\ntdeviceiocontrolfile.htm
ms.date: 12/05/2018
ms.keywords: NtDeviceIoControlFile, NtDeviceIoControlFile function [Windows API], winprog.ntdeviceiocontrolfile, winternl/NtDeviceIoControlFile, winui.ntdeviceiocontrolfile
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtDeviceIoControlFile
 - winternl/NtDeviceIoControlFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtDeviceIoControlFile
---

# NtDeviceIoControlFile function


## -description

Deprecated. Builds descriptors for the supplied buffer(s) and
    passes the untyped data to the device driver associated with the file
    handle.  <b>NtDeviceIoControlFile</b> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.

## -parameters

### -param FileHandle [in]

Open file handle to the file or device to which the control information should be given.

### -param Event [in]

A handle to an event to be set to the <code>signaled</code> state when the operation completes. This parameter can be <b>NULL</b>.

### -param ApcRoutine [in]

Procedure to be invoked once the operation completes. This parameter can be <b>NULL</b>. For more information on Asynchronous Procedure Calls (APCs), see <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>.

### -param ApcContext [in]

A pointer to pass to <i>ApcRoutine</i> when the operation completes. This parameter is required if an <i>ApcRoutine</i> is specified.

### -param IoStatusBlock [out]

Variable to receive the final completion status and information about the operation. Service calls that return information return the length of the data that is written to the output buffer in the Information field of this variable.

### -param IoControlCode [in]

Code that indicates which device I/O control function is to be executed.

### -param InputBuffer [in]

A pointer to a buffer that contains the information to be given to the target device. This parameter can be <b>NULL</b>. This information is device-dependent.

### -param InputBufferLength [in]

Length of the <i>InputBuffer</i> in bytes. If the buffer is not supplied, then this value is ignored.

### -param OutputBuffer [out]

A pointer to a buffer that is to receive the device-dependent return information from the target device. This parameter can be <b>NULL</b>.

### -param OutputBufferLength [in]

Length of the <i>OutputBuffer</i> in bytes. If the buffer is not supplied, then this value is ignored.

## -returns

The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The control operation was properly queued to the I/O system. Once the operation completes, the status can be determined by examining the Status field of the I/O status block. 

</td>
</tr>
</table>

## -remarks

The <b>NtDeviceIoControlFile</b> service is a device-dependent interface that extends the control that applications have over various devices within the system. This API provides a consistent view of the input and output data to the system while still providing the application and the driver a device-dependent method of specifying a communications interface.
		

The type of access to the file that the caller needs is dependent on the actual operation being performed.

Once the service is complete the <i>Event</i>, if specified, is set to the <code>signaled</code> state. If no <i>Event</i> parameter is specified, then the file object specified by the <i>FileHandle</i> is set to the <code>signaled</code> state. If an <i>ApcRoutine</i> is specified, it is invoked with the <i>ApcContext</i> and the <i>IoStatusBlock</i> as its arguments.

Because there is no import library for this function, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>