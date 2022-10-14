---
UID: NF:winusb.WinUsb_GetCurrentFrameNumberAndQpc
title: WinUsb_GetCurrentFrameNumberAndQpc function (winusb.h)
description: The WinUsb_GetCurrentFrameNumberAndQpc function retrieves the system query performance counter (QPC) value synchronized with the frame and microframe.
helpviewer_keywords: ["WinUsb_GetCurrentFrameNumberAndQpc","WinUsb_GetCurrentFrameNumberAndQpc function [Buses]","buses.winusb_getcurrentframenumberandqpc","winusb/WinUsb_GetCurrentFrameNumberAndQpc"]
old-location: buses\winusb_getcurrentframenumberandqpc.htm
tech.root: buses
ms.assetid: 9D94408F-C1EE-4940-8D33-8C32F5DE7DC4
ms.date: 12/05/2018
ms.keywords: WinUsb_GetCurrentFrameNumberAndQpc, WinUsb_GetCurrentFrameNumberAndQpc function [Buses], buses.winusb_getcurrentframenumberandqpc, winusb/WinUsb_GetCurrentFrameNumberAndQpc
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
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinUsb_GetCurrentFrameNumberAndQpc
 - winusb/WinUsb_GetCurrentFrameNumberAndQpc
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
 - WinUsb_GetCurrentFrameNumberAndQpc
---

# WinUsb_GetCurrentFrameNumberAndQpc function


## -description

The <b>WinUsb_GetCurrentFrameNumberAndQpc</b> function retrieves the system query performance counter (QPC) value  synchronized with the  frame and microframe.

## -parameters

### -param InterfaceHandle [in]

An opaque handle retrieved in the previous call to <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

### -param FrameQpcInfo [in]

A pointer to a <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_frame_number_and_qpc_for_time_sync_information">USB_FRAME_NUMBER_AND_QPC_FOR_TIME_SYNC_INFORMATION</a> structure. On output, <b>CurrentQueryPerformanceCounter</b> set to the system QPC  value (in microseconds) predicted by the USB driver stack. Optionally, on input, the caller can specify a frame and microframe number for which to retrieve the QPC value. 

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

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_starttrackingfortimesync">WinUsb_StartTrackingForTimeSync</a>