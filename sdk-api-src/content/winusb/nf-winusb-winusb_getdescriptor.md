---
UID: NF:winusb.WinUsb_GetDescriptor
title: WinUsb_GetDescriptor function (winusb.h)
description: The WinUsb_GetDescriptor function returns the requested descriptor. This is a synchronous operation.
helpviewer_keywords: ["WinUsb_GetDescriptor","WinUsb_GetDescriptor function [Buses]","buses.winusb_getdescriptor","winusb/WinUsb_GetDescriptor","winusbfunc_abc6ce9f-1e6f-470f-8770-6376cc9ffebf.xml"]
old-location: buses\winusb_getdescriptor.htm
tech.root: buses
ms.assetid: 59393a8f-4da9-44fd-8380-bb97e50cdb51
ms.date: 12/05/2018
ms.keywords: WinUsb_GetDescriptor, WinUsb_GetDescriptor function [Buses], buses.winusb_getdescriptor, winusb/WinUsb_GetDescriptor, winusbfunc_abc6ce9f-1e6f-470f-8770-6376cc9ffebf.xml
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
 - WinUsb_GetDescriptor
 - winusb/WinUsb_GetDescriptor
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
 - WinUsb_GetDescriptor
---

# WinUsb_GetDescriptor function


## -description

The <b>WinUsb_GetDescriptor</b> function returns the requested descriptor. This is a synchronous operation.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. 

To retrieve the device or configuration descriptor, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

To retrieve the interface descriptor of the  first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

To retrieve the endpoint descriptor of an endpoint in the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

To retrieve descriptors of all other interfaces and their related endpoints, use the handle to the target interface, retrieved by  <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param DescriptorType [in]

A value that specifies the type of descriptor to return. This parameter corresponds to the <b>bDescriptorType</b> field of a standard device descriptor, whose values are described in the <i>Universal Serial Bus </i> specification. Some of these values are listed in the description of the <b>DescriptorType</b> member of the <a href="/windows-hardware/drivers/ddi/content/usb/ns-usb-_urb_control_descriptor_request">_URB_CONTROL_DESCRIPTOR_REQUEST</a> structure.

### -param Index [in]

The descriptor index. For an explanation of the descriptor index, see the <i>Universal Serial Bus</i> specification (www.usb.org).

### -param LanguageID [in]

A value that specifies the language identifier, if the requested descriptor is a string descriptor.

### -param Buffer [out]

A caller-allocated buffer that receives the requested descriptor.

### -param BufferLength [in]

The length, in bytes, of <i>Buffer</i>.

### -param LengthTransferred [out]

The number of bytes that were copied into <i>Buffer</i>.

## -returns

<b>WinUsb_GetDescriptor</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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

If the output buffer pointed to by  the  <i>Buffer</i> parameter is large enough, <b>WinUsb_GetDescriptor</b> creates a copy of the specified descriptor into the output buffer. No data is copied if the buffer is not large enough to hold descriptor data.  The descriptor is created during the <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a> call or it may be retrieved at this point from the device.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>



<a href="/windows-hardware/drivers/ddi/content/usb/ns-usb-_urb_control_descriptor_request">_URB_CONTROL_DESCRIPTOR_REQUEST</a>