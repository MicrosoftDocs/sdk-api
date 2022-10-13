---
UID: NF:winusb.WinUsb_SetCurrentAlternateSetting
title: WinUsb_SetCurrentAlternateSetting function (winusb.h)
description: The WinUsb_SetCurrentAlternateSetting function sets the alternate setting of an interface.
helpviewer_keywords: ["WinUsb_SetCurrentAlternateSetting","WinUsb_SetCurrentAlternateSetting function [Buses]","buses.winusb_setcurrentalternatesetting","winusb/WinUsb_SetCurrentAlternateSetting","winusbfunc_54d8b9ed-9a45-4fed-a61e-2ad2bb573028.xml"]
old-location: buses\winusb_setcurrentalternatesetting.htm
tech.root: buses
ms.assetid: 8826f440-c031-4af2-968d-bf13f515f020
ms.date: 12/05/2018
ms.keywords: WinUsb_SetCurrentAlternateSetting, WinUsb_SetCurrentAlternateSetting function [Buses], buses.winusb_setcurrentalternatesetting, winusb/WinUsb_SetCurrentAlternateSetting, winusbfunc_54d8b9ed-9a45-4fed-a61e-2ad2bb573028.xml
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinUsb_SetCurrentAlternateSetting
 - winusb/WinUsb_SetCurrentAlternateSetting
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
 - WinUsb_SetCurrentAlternateSetting
---

# WinUsb_SetCurrentAlternateSetting function


## -description

The <b>WinUsb_SetCurrentAlternateSetting</b> function sets the alternate setting of an interface.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface, which defines the alternate setting to set. 

To set an alternate setting in the first interface on the device, use the interface handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param SettingNumber [in]

The value that is contained in the <b>bAlternateSetting</b> member of the <a href="/windows-hardware/drivers/ddi/content/usbspec/ns-usbspec-_usb_interface_descriptor">USB_INTERFACE_DESCRIPTOR</a> structure. This structure is populated by the <a href="/windows/desktop/api/winusb/nf-winusb-winusb_queryinterfacesettings">WinUsb_QueryInterfaceSettings</a> routine.

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

<a href="/windows-hardware/drivers/ddi/content/usbspec/ns-usbspec-_usb_interface_descriptor">USB_INTERFACE_DESCRIPTOR</a>



<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_queryinterfacesettings">WinUsb_QueryInterfaceSettings</a>