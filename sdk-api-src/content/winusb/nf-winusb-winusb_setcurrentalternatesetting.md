---
UID: NF:winusb.WinUsb_SetCurrentAlternateSetting
title: WinUsb_SetCurrentAlternateSetting function
author: windows-driver-content
description: The WinUsb_SetCurrentAlternateSetting function sets the alternate setting of an interface.
old-location: buses\winusb_setcurrentalternatesetting.htm
old-project: usbref
ms.assetid: 8826f440-c031-4af2-968d-bf13f515f020
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: WinUsb_SetCurrentAlternateSetting, WinUsb_SetCurrentAlternateSetting function [Buses], buses.winusb_setcurrentalternatesetting, winusb/WinUsb_SetCurrentAlternateSetting, winusbfunc_54d8b9ed-9a45-4fed-a61e-2ad2bb573028.xml
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
-	WinUsb_SetCurrentAlternateSetting
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_SetCurrentAlternateSetting function


## -description


The <b>WinUsb_SetCurrentAlternateSetting</b> function sets the alternate setting of an interface.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface, which defines the alternate setting to set. 

To set an alternate setting in the first interface on the device, use the interface handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540245">WinUsb_GetAssociatedInterface</a>.


### -param SettingNumber

TBD




#### - AlternateSetting [in]

The value that is contained in the <b>bAlternateSetting</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540065">USB_INTERFACE_DESCRIPTOR</a> structure. This structure is populated by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540292">WinUsb_QueryInterfaceSettings</a> routine.


## -returns



<b>WinUsb_SetCurrentAlternateSetting</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
 




## -remarks



<b>WinUsb_SetCurrentAlternateSetting</b> fails if outstanding I/O requests are present on the interface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540065">USB_INTERFACE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540292">WinUsb_QueryInterfaceSettings</a>
 

 

