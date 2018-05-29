---
UID: NF:winusb.WinUsb_GetCurrentFrameNumber
title: WinUsb_GetCurrentFrameNumber function
author: windows-sdk-content
description: The WinUsb_GetCurrentFrameNumber function gets the current frame number for the bus.
old-location: buses\winusb_getcurrentframenumber.htm
old-project: usbref
ms.assetid: 178E1679-B78F-4032-8D1B-66B7ABE902C7
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WinUsb_GetCurrentFrameNumber, WinUsb_GetCurrentFrameNumber routine [Buses], buses.winusb_getcurrentframenumber, winusb/WinUsb_GetCurrentFrameNumber
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
-	WinUsb_GetCurrentFrameNumber
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_GetCurrentFrameNumber function


## -description


The <b>WinUsb_GetCurrentFrameNumber</b> function gets the current frame number for the bus.


## -parameters




### -param InterfaceHandle

TBD


### -param CurrentFrameNumber [out]

The current frame number value.


### -param TimeStamp [out]

The time stamp value when the current frame was read.


#### - DeviceHandle [in]

The handle to the device that <b>CreateFile</b> returned.


## -returns



<b>WinUsb_GetCurrentFrameNumber</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.




## -remarks



The caller may compare the PerformanceCount with the value returned by the Win32 function <a href="https://msdn.microsoft.com/08169390-940b-4110-813a-249d107cc953">QueryPerformanceCounter</a> to determine if there has been a delay in transitioning back to user-mode after the frame number was read.  The caller can then adjust the starting frame number as needed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn376866">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>
 

 

