---
UID: NF:winusb.WinUsb_UnregisterIsochBuffer
title: WinUsb_UnregisterIsochBuffer function (winusb.h)
author: windows-sdk-content
description: The WinUsb_UnregisterIsochBuffer function releases all of the resources that WinUsb_RegisterIsochBuffer allocated for isochronous transfers. This is a synchronous operation.
old-location: buses\winusb_unregisterisochbuffer.htm
tech.root: usbref
ms.assetid: 1BAD13F5-A29E-4BA8-B924-85ACE7C8E34D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WinUsb_UnregisterIsochBuffer, WinUsb_UnregisterIsochBuffer function [Buses], buses.winusb_unregisterisochbuffer, winusb/WinUsb_UnregisterIsochBuffer
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
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_UnregisterIsochBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinUsb_UnregisterIsochBuffer function


## -description


The <b>WinUsb_UnregisterIsochBuffer</b> function releases all of the resources that <a href="https://msdn.microsoft.com/7781BD59-3576-4C43-9459-E2455F97E9DE">WinUsb_RegisterIsochBuffer</a> allocated for isochronous transfers. This is a synchronous operation.


## -parameters




### -param IsochBufferHandle [in]

An opaque handle to the transfer buffer that was registered by a previous call to <a href="https://msdn.microsoft.com/7781BD59-3576-4C43-9459-E2455F97E9DE">WinUsb_RegisterIsochBuffer</a>. 


## -returns



<b>WinUsb_UnregisterIsochBuffer</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.




## -remarks



The caller must ensure that there are no pending transfers that is currently using the buffer before calling <b>WinUsb_UnregisterIsochBuffer</b>.  If there are pending transfers, <b>WinUsb_UnregisterIsochBuffer</b> blocks until those transfers are complete.




## -see-also




<a href="https://msdn.microsoft.com/E850ACF2-7FF7-42A2-B3FA-3CFE3A3968E3">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/7781BD59-3576-4C43-9459-E2455F97E9DE">WinUsb_RegisterIsochBuffer</a>
 

 

