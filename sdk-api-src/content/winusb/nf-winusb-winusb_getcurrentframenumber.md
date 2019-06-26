---
UID: NF:winusb.WinUsb_GetCurrentFrameNumber
title: WinUsb_GetCurrentFrameNumber function (winusb.h)
author: windows-sdk-content
description: The WinUsb_GetCurrentFrameNumber function gets the current frame number for the bus.
old-location: buses\winusb_getcurrentframenumber.htm
tech.root: usbref
ms.assetid: 178E1679-B78F-4032-8D1B-66B7ABE902C7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WinUsb_GetCurrentFrameNumber, WinUsb_GetCurrentFrameNumber function [Buses], buses.winusb_getcurrentframenumber, winusb/WinUsb_GetCurrentFrameNumber
ms.topic: function
f1_keywords: 
 - "winusb/WinUsb_GetCurrentFrameNumber"
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
 - WinUsb_GetCurrentFrameNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WinUsb_GetCurrentFrameNumber function


## -description


The <b>WinUsb_GetCurrentFrameNumber</b> function gets the current frame number for the bus.


## -parameters




### -param InterfaceHandle [in]

The handle to the device that <b>CreateFile</b> returned.


### -param CurrentFrameNumber [out]

The current frame number value.


### -param TimeStamp [out]

The time stamp value when the current frame was read.


## -returns



<b>WinUsb_GetCurrentFrameNumber</b> returns TRUE if the operation succeeds.  Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.




## -remarks



The caller may compare the PerformanceCount with the value returned by the Win32 function <a href="https://docs.microsoft.com/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> to determine if there has been a delay in transitioning back to user-mode after the frame number was read.  The caller can then adjust the starting frame number as needed.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/usbcon/">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>
 

 

