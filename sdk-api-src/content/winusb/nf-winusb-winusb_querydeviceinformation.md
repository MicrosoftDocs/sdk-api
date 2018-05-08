---
UID: NF:winusb.WinUsb_QueryDeviceInformation
title: WinUsb_QueryDeviceInformation function
author: windows-driver-content
description: The WinUsb_QueryDeviceInformation function gets information about the physical device that is associated with a WinUSB interface handle.
old-location: buses\winusb_querydeviceinformation.htm
old-project: usbref
ms.assetid: 0d77c41c-2d3d-41c9-b8f9-054c5e622a5a
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: WinUsb_QueryDeviceInformation, WinUsb_QueryDeviceInformation function [Buses], buses.winusb_querydeviceinformation, winusb/WinUsb_QueryDeviceInformation, winusbfunc_db8c1496-f45c-4d74-b786-8822692aafd9.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	WinUsb_QueryDeviceInformation
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_QueryDeviceInformation function


## -description


The <b>WinUsb_QueryDeviceInformation</b> function gets information about the physical device that is associated with a WinUSB interface handle.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to the first interface on the device, which is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>. 


### -param InformationType [in]

A value that specifies which interface information value to retrieve.

On input, <i>InformationType</i> must have the following value: DEVICE_SPEED (0x01). 


### -param BufferLength [in, out]

The maximum number of bytes to read. This number must be less than or equal to the size, in bytes, of <i>Buffer</i>. On output, <i>BufferLength</i> is set to the actual number of bytes that were copied into <i>Buffer</i>.


### -param Buffer [out]

A caller-allocated buffer that receives the requested value.

If <i>InformationType</i> is DEVICE_SPEED, on successful return, <i>Buffer</i> indicates the operating speed of the device. 0x03 indicates high-speed or higher; 0x01 indicates full-speed or lower.


## -returns



<b>WinUsb_QueryDeviceInformation</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


<b>GetLastError</b>    can return the following error code.



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
The caller passed <b>NULL</b> in the  <i>InterfaceHandle</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>
 

 

