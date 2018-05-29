---
UID: NF:winusb.WinUsb_GetAdjustedFrameNumber
title: WinUsb_GetAdjustedFrameNumber function
author: windows-sdk-content
description: The WinUsb_GetAdjustedFrameNumber function computes what the current USB frame number should be based on the frame number value and timestamp.
old-location: buses\winusb_getadjustedframenumber.htm
old-project: usbref
ms.assetid: 4FB5D8D5-992C-49D2-87FE-FA1F34D98D70
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WinUsb_GetAdjustedFrameNumber, WinUsb_GetAdjustedFrameNumber routine [Buses], buses.winusb_getadjustedframenumber, winusb/WinUsb_GetAdjustedFrameNumber
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
-	WinUsb_GetAdjustedFrameNumber
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_GetAdjustedFrameNumber function


## -description


The <b>WinUsb_GetAdjustedFrameNumber</b> function computes what the current USB frame number should be based      on the frame number value and timestamp.  


## -parameters




### -param CurrentFrameNumber [in, out]

The frame number to be adjusted.


### -param TimeStamp [in]

The timestamp recorded at the time the frame        number was returned.                                         


## -returns



<b>WinUsb_GetAdjustedFrameNumber</b> returns TRUE if the operation succeeds. Otherwise this function returns FALSE, and the caller can retrieve the logged error by calling <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn376866">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>
 

 

