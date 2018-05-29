---
UID: NF:winusb.WinUsb_RegisterIsochBuffer
title: WinUsb_RegisterIsochBuffer function
author: windows-sdk-content
description: The WinUsb_RegisterIsochBuffer function registers a buffer to be used for isochronous transfers.
old-location: buses\winusb_registerisochbuffer.htm
old-project: usbref
ms.assetid: 7781BD59-3576-4C43-9459-E2455F97E9DE
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WinUsb_RegisterIsochBuffer, WinUsb_RegisterIsochBuffer routine [Buses], buses.winusb_registerisochbuffer, winusb/WinUsb_RegisterIsochBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WIN_CERTIFICATE, *LPWIN_CERTIFICATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winusb.dll
api_name:
-	WinUsb_RegisterIsochBuffer
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_RegisterIsochBuffer function


## -description


The <b>WinUsb_RegisterIsochBuffer</b> function registers a buffer to be used for isochronous transfers.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. That handle must be created by a previous call to  <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff540245">WinUsb_GetAssociatedInterface</a>.


### -param PipeID [in]

Derived from Bit 3...0 of the <b>bEndpointAddress</b> field in the endpoint descriptor.


### -param Buffer [in]

Pointer to the transfer buffer to be registered.


### -param BufferLength [in]

Length, in bytes, of the transfer buffer pointed to by <i>Buffer</i>.


### -param IsochBufferHandle

TBD




#### - BufferHandle [out]

Receives an opaque handle to the registered buffer. This handle is required by other WinUSB functions that perform isochronous transfers. To release the handle, call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265567">WinUsb_UnregisterIsochBuffer</a> function.


## -returns



<b>WinUsb_RegisterIsochBuffer</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.

If the caller sets <i>ContinueStream</i> to TRUE, The transfer fails if Winusb.sys is unable to schedule the transfer to continue the stream without dropping one or more frames.




## -remarks



Prior to initiating isochronous transfers to or from a buffer, the caller must register the buffer with <b>WinUsb_RegisterIsochBuffer</b>.  This call allows the Winusb.sys to pre-map and lock the buffer after for all subsequent transfers using the buffer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn376866">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265567">WinUsb_UnregisterIsochBuffer</a>
 

 

