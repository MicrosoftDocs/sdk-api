---
UID: NF:winusb.WinUsb_RegisterIsochBuffer
title: WinUsb_RegisterIsochBuffer function (winusb.h)
description: The WinUsb_RegisterIsochBuffer function registers a buffer to be used for isochronous transfers.
helpviewer_keywords: ["WinUsb_RegisterIsochBuffer","WinUsb_RegisterIsochBuffer function [Buses]","buses.winusb_registerisochbuffer","winusb/WinUsb_RegisterIsochBuffer"]
old-location: buses\winusb_registerisochbuffer.htm
tech.root: buses
ms.assetid: 7781BD59-3576-4C43-9459-E2455F97E9DE
ms.date: 12/05/2018
ms.keywords: WinUsb_RegisterIsochBuffer, WinUsb_RegisterIsochBuffer function [Buses], buses.winusb_registerisochbuffer, winusb/WinUsb_RegisterIsochBuffer
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
 - WinUsb_RegisterIsochBuffer
 - winusb/WinUsb_RegisterIsochBuffer
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
 - WinUsb_RegisterIsochBuffer
---

# WinUsb_RegisterIsochBuffer function


## -description

The <b>WinUsb_RegisterIsochBuffer</b> function registers a buffer to be used for isochronous transfers.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. That handle must be created by a previous call to  <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a> or <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param PipeID [in]

Derived from Bit 3...0 of the <b>bEndpointAddress</b> field in the endpoint descriptor.

### -param Buffer [in]

Pointer to the transfer buffer to be registered.

### -param BufferLength [in]

Length, in bytes, of the transfer buffer pointed to by <i>Buffer</i>.

### -param IsochBufferHandle [out]

Receives an opaque handle to the registered buffer. This handle is required by other WinUSB functions that perform isochronous transfers. To release the handle, call the <a href="/windows/desktop/api/winusb/nf-winusb-winusb_unregisterisochbuffer">WinUsb_UnregisterIsochBuffer</a> function.

## -returns

<b>WinUsb_RegisterIsochBuffer</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.

If the caller sets <i>ContinueStream</i> to TRUE, The transfer fails if Winusb.sys is unable to schedule the transfer to continue the stream without dropping one or more frames.

## -remarks

Prior to initiating isochronous transfers to or from a buffer, the caller must register the buffer with <b>WinUsb_RegisterIsochBuffer</b>.  This call allows the Winusb.sys to pre-map and lock the buffer after for all subsequent transfers using the buffer.

## -see-also

<a href="/windows-hardware/drivers/usbcon/">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_unregisterisochbuffer">WinUsb_UnregisterIsochBuffer</a>