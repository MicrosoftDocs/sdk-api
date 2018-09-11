---
UID: NF:winusb.WinUsb_GetCurrentAlternateSetting
title: WinUsb_GetCurrentAlternateSetting function
author: windows-sdk-content
description: The WinUsb_GetCurrentAlternateSetting function gets the current alternate interface setting for an interface. This is a synchronous operation.
old-location: buses\winusb_getcurrentalternatesetting.htm
tech.root: usbref
ms.assetid: a644eb68-2192-4927-ac67-77384f8cf2b6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WinUsb_GetCurrentAlternateSetting, WinUsb_GetCurrentAlternateSetting function [Buses], buses.winusb_getcurrentalternatesetting, winusb/WinUsb_GetCurrentAlternateSetting, winusbfunc_26a4514e-edde-432d-aac7-c4d2466c70c3.xml
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
 - WinUsb_GetCurrentAlternateSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinUsb_GetCurrentAlternateSetting function


## -description


The <b>WinUsb_GetCurrentAlternateSetting</b> function gets the current alternate interface setting for an interface. This is a synchronous operation.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. To get the current alternate setting in the first (default) interface on the device, use the interface handle returned by <a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/1afc7b2f-4fb6-4ab4-8415-aaee9cd6ee0c">WinUsb_GetAssociatedInterface</a>.


### -param SettingNumber [out]

A pointer to an unsigned character that receives an integer that indicates the current alternate setting.


## -returns



<b>WinUsb_GetCurrentAlternateSetting</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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



<a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>
 

 

