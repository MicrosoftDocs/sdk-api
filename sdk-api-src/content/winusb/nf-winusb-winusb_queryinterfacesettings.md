---
UID: NF:winusb.WinUsb_QueryInterfaceSettings
title: WinUsb_QueryInterfaceSettings function (winusb.h)
author: windows-sdk-content
description: The WinUsb_QueryInterfaceSettings function retrieves the interface descriptor for the specified alternate interface settings for a particular interface handle.
old-location: buses\winusb_queryinterfacesettings.htm
tech.root: usbref
ms.assetid: fe36e441-60eb-4df3-8100-6c441c599a60
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WinUsb_QueryInterfaceSettings, WinUsb_QueryInterfaceSettings function [Buses], buses.winusb_queryinterfacesettings, winusb/WinUsb_QueryInterfaceSettings, winusbfunc_e69535c0-faad-4708-823c-f343e8ae2e9d.xml
ms.topic: function
f1_keywords: 
 - "winusb/WinUsb_QueryInterfaceSettings"
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
 - WinUsb_QueryInterfaceSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WinUsb_QueryInterfaceSettings function


## -description


The <b>WinUsb_QueryInterfaceSettings</b> function retrieves the interface descriptor for the specified alternate interface settings for a particular interface handle.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. 

To retrieve the settings of the first interface, use the handle returned by <a href="https://docs.microsoft.com/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.


### -param AlternateInterfaceNumber [in]

A value that indicates which alternate settings to return. A value of 0 indicates the first alternate setting, a value of 1 indicates the second alternate setting, and so on.


### -param UsbAltInterfaceDescriptor [out]

A pointer to a caller-allocated <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usbspec/ns-usbspec-_usb_interface_descriptor">USB_INTERFACE_DESCRIPTOR</a> structure that contains information about the interface that <i>AlternateSettingNumber</i> specified.


## -returns



<b>WinUsb_QueryInterfaceSettings</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, it returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The specified alternate interface was not found.

</td>
</tr>
</table>
 




## -remarks



<b>WinUsb_QueryInterfaceSettings</b> parses the configuration descriptor previously retrieved by  <a href="https://docs.microsoft.com/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For more information, see the Remarks section for <b>WinUsb_Initialize</b>. 

The <b>WinUsb_QueryInterfaceSettings</b> call searches the interface array for the alternate interface specified by the interface index passed by the caller in the <i>AlternateSettingNumber</i>. If the specified interface is found, the function populates the caller-allocated <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usbspec/ns-usbspec-_usb_interface_descriptor">USB_INTERFACE_DESCRIPTOR</a> structure. If the specified interface is not found, then the call fails with the ERROR_NO_MORE_ITEMS code.






## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usbspec/ns-usbspec-_usb_interface_descriptor">USB_INTERFACE_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>
 

 

