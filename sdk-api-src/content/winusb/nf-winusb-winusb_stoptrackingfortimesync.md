---
UID: NF:winusb.WinUsb_StopTrackingForTimeSync
title: WinUsb_StopTrackingForTimeSync function (winusb.h)
description: The WinUsb_StopTrackingForTimeSync function tops the time synchronization feature in the USB driver stack that gets the associated system QPC time for USB bus frames and microframes.
helpviewer_keywords: ["WinUsb_StopTrackingForTimeSync","WinUsb_StopTrackingForTimeSync function [Buses]","buses.winusb_stoptrackingfortimesync","winusb/WinUsb_StopTrackingForTimeSync"]
old-location: buses\winusb_stoptrackingfortimesync.htm
tech.root: buses
ms.assetid: F38DBE34-A6D0-4492-A829-EFE53D361A71
ms.date: 12/05/2018
ms.keywords: WinUsb_StopTrackingForTimeSync, WinUsb_StopTrackingForTimeSync function [Buses], buses.winusb_stoptrackingfortimesync, winusb/WinUsb_StopTrackingForTimeSync
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
 - WinUsb_StopTrackingForTimeSync
 - winusb/WinUsb_StopTrackingForTimeSync
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
 - WinUsb_StopTrackingForTimeSync
---

# WinUsb_StopTrackingForTimeSync function


## -description

The <b>WinUsb_StopTrackingForTimeSync</b> function stops the time synchronization feature in the USB driver stack that gets the associated system QPC time for USB bus frames and microframes.

## -parameters

### -param InterfaceHandle [in]

An opaque handle retrieved in the previous call to <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

### -param StopTrackingInfo [in]

A pointer to a <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_stop_tracking_for_time_sync_information">USB_STOP_TRACKING_FOR_TIME_SYNC_INFORMATION</a> structure. Set <b>TimeTrackingHandle</b> to the handle received in the previous call to <a href="/windows/desktop/api/winusb/nf-winusb-winusb_starttrackingfortimesync">WinUsb_StartTrackingForTimeSync</a>.

## -returns

<b>WinUsb_StopTrackingForTimeSync</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
The caller passed <b>NULL</b> in the  <i>InterfaceHandle</i> or <i>StopTrackingInfo</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_starttrackingfortimesync">WinUsb_StartTrackingForTimeSync</a>
