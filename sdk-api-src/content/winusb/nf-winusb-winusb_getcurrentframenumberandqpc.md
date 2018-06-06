---
UID: NF:winusb.WinUsb_GetCurrentFrameNumberAndQpc
title: WinUsb_GetCurrentFrameNumberAndQpc function
author: windows-sdk-content
description: The WinUsb_GetCurrentFrameNumberAndQpc function retrieves the system query performance counter (QPC) value synchronized with the frame and microframe.
old-location: buses\winusb_getcurrentframenumberandqpc.htm
old-project: usbref
ms.assetid: 9D94408F-C1EE-4940-8D33-8C32F5DE7DC4
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WinUsb_GetCurrentFrameNumberAndQpc, WinUsb_GetCurrentFrameNumberAndQpc function [Buses], buses.winusb_getcurrentframenumberandqpc, winusb/WinUsb_GetCurrentFrameNumberAndQpc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WIN_CERTIFICATE, *LPWIN_CERTIFICATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_GetCurrentFrameNumberAndQpc
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_GetCurrentFrameNumberAndQpc function


## -description


The <b>WinUsb_GetCurrentFrameNumberAndQpc</b> function retrieves the system query performance counter (QPC) value  synchronized with the  frame and microframe.


## -parameters




### -param InterfaceHandle [in]

An opaque handle retrieved in the previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>. 


### -param FrameQpcInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/F602B738-4D04-4A75-BE69-CFEC4F76904C">USB_FRAME_NUMBER_AND_QPC_FOR_TIME_SYNC_INFORMATION</a> structure. On output, <b>CurrentQueryPerformanceCounter</b> set to the system QPC  value (in microseconds) predicted by the USB driver stack. Optionally, on input, the caller can specify a frame and microframe number for which to retrieve the QPC value. 

On output, the <b>QueryPerformanceCounterAtInputFrameOrMicroFrame</b> member  is set to the QPC value for that frame or microframe.


## -returns



<b>WinUsb_GetCurrentFrameNumberAndQpc</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


<b>GetLastError</b>    can return one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The caller passed <b>NULL</b> in the  <i>InterfaceHandle</i> or <i>FrameQpcInfo</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>



<a href="https://msdn.microsoft.com/FC19CDFD-76F1-49E3-A212-E4F490D679E6">WinUsb_StartTrackingForTimeSync</a>
 

 

