---
UID: NF:winusb.WinUsb_GetOverlappedResult
title: WinUsb_GetOverlappedResult function (winusb.h)
description: The WinUsb_GetOverlappedResult function retrieves the results of an overlapped operation on the specified file.
helpviewer_keywords: ["WinUsb_GetOverlappedResult","WinUsb_GetOverlappedResult function [Buses]","buses.winusb_getoverlappedresult","winusb/WinUsb_GetOverlappedResult","winusbfunc_197c2ea2-c5fd-4a19-b4e5-00c373231606.xml"]
old-location: buses\winusb_getoverlappedresult.htm
tech.root: buses
ms.assetid: e6078b1f-0921-4e1f-a444-f8a1481c8f8a
ms.date: 12/05/2018
ms.keywords: WinUsb_GetOverlappedResult, WinUsb_GetOverlappedResult function [Buses], buses.winusb_getoverlappedresult, winusb/WinUsb_GetOverlappedResult, winusbfunc_197c2ea2-c5fd-4a19-b4e5-00c373231606.xml
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
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
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinUsb_GetOverlappedResult
 - winusb/WinUsb_GetOverlappedResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_GetOverlappedResult
---

# WinUsb_GetOverlappedResult function


## -description

The <b>WinUsb_GetOverlappedResult</b> function retrieves the results of an overlapped operation on the specified file.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to the first interface on the device, which is returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

### -param lpOverlapped [in]

A pointer to an <b>OVERLAPPED</b> structure that was specified when the overlapped operation was started.

### -param lpNumberOfBytesTransferred [out]

A pointer to a variable that receives the number of bytes that were actually transferred by a read or write operation.

### -param bWait [in]

If this parameter is <b>TRUE</b>, the function does not return until the operation has been completed. If this parameter is <b>FALSE</b> and the operation is still pending, the function returns <b>FALSE</b> and the <b>GetLastError</b> function returns ERROR_IO_INCOMPLETE.

## -returns

If the function succeeds, the return value is any number other than zero. If the function fails, the return value is zero. To get extended error information, call <b>GetLastError</b>.

## -remarks

This function is like the Win32 API routine, <b>GetOverlappedResult</b>, with one difference—instead of passing a file handle that is returned from <b>CreateFile</b>, the caller passes an interface handle that is returned from <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. The caller can use either API routine, if the appropriate handle is passed. The <b>WinUsb_GetOverlappedResult </b> function extracts the file handle from the interface handle and then calls <b>GetOverlappedResult</b>.

The results that are reported by the <b>WinUsb_GetOverlappedResult</b> function are those from the specified handle's last overlapped operation to which the specified <b>OVERLAPPED</b> structure was provided, and for which the operation's results were pending. A pending operation is indicated when the function that started the operation returns <b>FALSE</b>, and the <b>GetLastError</b> routine returns ERROR_IO_PENDING. When an I/O operation is pending, the function that started the operation resets the <b>hEvent</b> member of the <b>OVERLAPPED</b> structure to the nonsignaled state. Then when the pending operation has been completed, the system sets the event object to the signaled state.

The caller can specify that an event object is manually reset in the <b>OVERLAPPED</b> structure. If an automatic reset event object is used, the event handle must not be specified in any other wait operation in the interval between starting the overlapped operation and the call to <b>WinUsb_GetOverlappedResult</b>. For example, the event object is sometimes specified in one of the wait routines to wait for the operation to be completed. When the wait routine returns, the system sets an auto-reset event's state to nonsignaled, and a successive call to <b>WinUsb_GetOverlappedResult</b> with the <i>bWait</i> parameter set to <b>TRUE</b> causes the function to be blocked indefinitely.

If the <i>bWait</i> parameter is <b>TRUE</b>, <b>WinUsb_GetOverlappedResult</b> determines whether the pending operation has been completed by waiting for the event object to be in the signaled state.

If the <b>hEvent</b> member of the <b>OVERLAPPED</b> structure is <b>NULL</b>, the system uses the state of the file handle to signal when the operation has been completed. Do not use file handles for this purpose. It is better to use an event object because of the confusion that can occur when multiple concurrent overlapped operations are performed on the same file. In this situation, you cannot know which operation caused the state of the object to be signaled.

## -see-also

<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>



<a href="/windows-hardware/drivers/ddi/content/usb/ns-usb-_urb_control_descriptor_request">_URB_CONTROL_DESCRIPTOR_REQUEST</a>