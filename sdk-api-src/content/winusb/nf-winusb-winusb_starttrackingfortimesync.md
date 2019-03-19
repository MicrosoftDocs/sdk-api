---
UID: NF:winusb.WinUsb_StartTrackingForTimeSync
title: WinUsb_StartTrackingForTimeSync function (winusb.h)
author: windows-sdk-content
description: The WinUsb_StartTrackingForTimeSync function starts the time synchronization feature in the USB driver stack that gets the associated system QPC time for USB bus frames and microframes.
old-location: buses\winusb_starttrackingfortimesync.htm
tech.root: usbref
ms.assetid: FC19CDFD-76F1-49E3-A212-E4F490D679E6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WinUsb_StartTrackingForTimeSync, WinUsb_StartTrackingForTimeSync function [Buses], buses.winusb_starttrackingfortimesync, winusb/WinUsb_StartTrackingForTimeSync
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
 - WinUsb_StartTrackingForTimeSync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinUsb_StartTrackingForTimeSync function


## -description


The <b>WinUsb_StartTrackingForTimeSync</b> function starts the time synchronization feature in the USB driver stack that gets the associated system QPC time for USB bus frames and microframes. 


## -parameters




### -param InterfaceHandle [in]

An opaque handle retrieved in the previous call to <a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>. 


### -param StartTrackingInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/2C82743C-2675-4196-839D-885EE17B2A7A">USB_START_TRACKING_FOR_TIME_SYNC_INFORMATION</a> structure. Set <b>TimeTrackingHandle</b> to INAVLID_HANDLE.
Set <b>IsStartupDelayTolerable</b> to TRUE if the initial startup latency of up to 2.048 seconds is tolerable. FALSE, the registration is delayed until the USB driver stack is able to detect a valid frame or microframe boundary. 




## -returns



<b>WinUsb_StartTrackingForTimeSync</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
The caller passed <b>NULL</b> in the  <i>InterfaceHandle</i> or <i>StartTrackingInfo</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>
 

 

