---
UID: NF:winusb.WinUsb_WriteIsochPipeAsap
title: WinUsb_WriteIsochPipeAsap function (winusb.h)
description: The WinUsb_WriteIsochPipeAsap submits a request for writing the contents of a buffer to an isochronous OUT endpoint.
helpviewer_keywords: ["WinUsb_WriteIsochPipeAsap","WinUsb_WriteIsochPipeAsap function [Buses]","buses.winusb_writeisochpipeasap","winusb/WinUsb_WriteIsochPipeAsap"]
old-location: buses\winusb_writeisochpipeasap.htm
tech.root: buses
ms.assetid: CC8776DF-9DC6-4B75-A4CE-EAC644EABABA
ms.date: 12/05/2018
ms.keywords: WinUsb_WriteIsochPipeAsap, WinUsb_WriteIsochPipeAsap function [Buses], buses.winusb_writeisochpipeasap, winusb/WinUsb_WriteIsochPipeAsap
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
 - WinUsb_WriteIsochPipeAsap
 - winusb/WinUsb_WriteIsochPipeAsap
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
 - WinUsb_WriteIsochPipeAsap
---

# WinUsb_WriteIsochPipeAsap function


## -description

The <b>WinUsb_WriteIsochPipeAsap</b> submits a request for writing the contents of a buffer to an isochronous OUT endpoint.

## -parameters

### -param BufferHandle [in]

An opaque handle to the transfer buffer that was registered by a previous call to <a href="/windows/desktop/api/winusb/nf-winusb-winusb_registerisochbuffer">WinUsb_RegisterIsochBuffer</a>.

### -param Offset [in]

Offset into the buffer relative to the start the transfer.

### -param Length [in]

Length in bytes of the transfer buffer.

### -param ContinueStream [in]

Indicates that the transfer should only be submitted if it can be scheduled in the first frame after the last pending transfer.

### -param Overlapped [in, optional]

Pointer to an <a href="/windows/desktop/api/shobjidl/ns-shobjidl-overlapped">OVERLAPPED</a> structure used for asynchronous operations.

## -returns

<b>WinUsb_WriteIsochPipeAsap</b> returns TRUE if the operation succeeds. Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.

If the caller sets <i>ContinueStream</i> to TRUE, The transfer fails if Winusb.sys is unable to schedule the transfer to continue the stream without dropping one or more frames.

## -remarks

<b>WinUsb_WriteIsochPipeAsap</b> allows the USB driver stack to choose the starting frame number for the transfer. If one or more transfers are already pending on the endpoint, the transfer will be scheduled for the frame number immediately following the last frame number of the last currently pending transfer.


<b>WinUsb_WriteIsochPipeAsap</b> packetizes the transfer buffer so that in each 1ms interval, the host can send the maximum bytes allowed per interval. The maximum bytes is as specified by the endpoint descriptor for full and high-speed endpoints, and endpoint companion descriptor for SuperSpeed endpoints.
If the caller submits multiple write requests to stream data to the device, the transfer size should be a multiple of the maximum bytes per interval (as returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_querypipeex">WinUsb_QueryPipeEx</a>) * 8 / interval.


Because of the transfer packaging used in the underlying kernel-mode interface, the lowest latency notification to an application or driver is 1ms intervals.

## -see-also

<a href="/windows-hardware/drivers/usbcon/">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>