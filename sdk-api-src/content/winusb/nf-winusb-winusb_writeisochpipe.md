---
UID: NF:winusb.WinUsb_WriteIsochPipe
title: WinUsb_WriteIsochPipe function
author: windows-sdk-content
description: The WinUsb_WriteIsochPipe function writes the contents of a caller-supplied buffer to an isochronous OUT endpoint, starting on a specified frame number.
old-location: buses\winusb_writeisochpipe.htm
old-project: usbref
ms.assetid: E5185806-F447-49A8-BEC9-B85451E78533
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WinUsb_WriteIsochPipe, WinUsb_WriteIsochPipe routine [Buses], buses.winusb_writeisochpipe, winusb/WinUsb_WriteIsochPipe
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
-	WinUsb_WriteIsochPipe
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_WriteIsochPipe function


## -description


The <b>WinUsb_WriteIsochPipe</b> function writes the contents of a caller-supplied buffer to an isochronous OUT endpoint, starting on a specified frame number.  


## -parameters




### -param BufferHandle [in]

An opaque handle to the transfer buffer that was registered by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/dn265566">WinUsb_RegisterIsochBuffer</a>. 


### -param Offset [in]

Offset into the buffer relative to the start the transfer.


### -param Length [in]

Length in bytes of the transfer buffer.


### -param FrameNumber [in, out]

On input, indicates the starting frame number for the transfer.  On output, contains the frame number of the frame that follows the last frame used in the transfer.


### -param Overlapped [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/2b5964e5-dfc8-44f9-86a7-5ea5acc68c1b">OVERLAPPED</a> structure used for asynchronous operations.


## -returns



<b>WinUsb_WriteIsochPipe</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.




## -remarks



<b>WinUsb_WriteIsochPipe</b> packetizes the transfer buffer so that in each interval,  the host can send the maximum bytes allowed per interval. The maximum bytes is as specified by the endpoint descriptor for full and high-speed endpoints, and endpoint companion descriptor for SuperSpeed endpoints.
If the caller submits multiple write requests to stream data to the device, the transfer size should be a multiple of the maximum bytes per interval (as returned by <a href="https://msdn.microsoft.com/library/windows/hardware/dn265563">WinUsb_QueryPipeEx</a>) * 8 / interval.





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn376866">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>
 

 

