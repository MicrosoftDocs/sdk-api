---
UID: NF:winusb.WinUsb_Initialize
title: WinUsb_Initialize function (winusb.h)
description: The WinUsb_Initialize function creates a WinUSB handle for the device specified by a file handle.
helpviewer_keywords: ["WinUsb_Initialize","WinUsb_Initialize function [Buses]","buses.winusb_initialize","winusb/WinUsb_Initialize","winusbfunc_f0a58fec-c4eb-49b7-81d0-89c891e10731.xml"]
old-location: buses\winusb_initialize.htm
tech.root: buses
ms.assetid: 258cf508-036a-4ade-95b2-4b36d1149ffd
ms.date: 12/05/2018
ms.keywords: WinUsb_Initialize, WinUsb_Initialize function [Buses], buses.winusb_initialize, winusb/WinUsb_Initialize, winusbfunc_f0a58fec-c4eb-49b7-81d0-89c891e10731.xml
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
 - WinUsb_Initialize
 - winusb/WinUsb_Initialize
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
 - WinUsb_Initialize
---

# WinUsb_Initialize function


## -description

The <b>WinUsb_Initialize</b> function creates a WinUSB handle for the device specified by a file handle.

## -parameters

### -param DeviceHandle [in]

The handle to the device that <b>CreateFile</b> returned. WinUSB uses overlapped I/O, so FILE_FLAG_OVERLAPPED must be specified in the <i>dwFlagsAndAttributes</i> parameter of <b>CreateFile</b> call for <i>DeviceHandle</i> to have the characteristics necessary for <b>WinUsb_Initialize</b> to function properly.

### -param InterfaceHandle [out]

Receives an opaque handle to the first (default) interface on the device. This handle is required by other WinUSB routines that perform operations on the default interface. To release the handle, call the <a href="/windows/desktop/api/winusb/nf-winusb-winusb_free">WinUSB_Free</a> function.

## -returns

<b>WinUsb_Initialize</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
The caller passed <b>NULL</b> or an invalid handle in the  <i>DeviceHandle</i> parameter; FILE_FLAG_OVERLAPPED was not set in the file handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there is insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the default interface descriptor could not be found for the device.

</td>
</tr>
</table>

## -remarks

When <b>WinUsb_Initialize</b> is called,
   the policy settings of the interface are reset to the default values. 

The <b>WinUsb_Initialize</b> call queries the underlying USB stack for various descriptors and allocates enough memory to store the retrieved descriptor data. 

<b>WinUsb_Initialize</b> first retrieves the device descriptor and then gets the associated configuration descriptor. From the configuration descriptor, the call derives the associated interface descriptors and stores them in an array. The interfaces in the array are identified by zero-based indexes. An index value of 0 indicates the first interface (the default interface), a value of 1 indicates the second associated interface, and so on.
    <b>WinUsb_Initialize</b> parses the default interface descriptor for the endpoint descriptors and caches information such as the associated pipes or state specific data.
The handle received in the <i>InterfaceHandle</i> parameter is a pointer to the memory block allocated for the first interface in the array. 

If an application wants to use another interface on the device, it must call <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>,  specify the index of the interface, and retrieve a handle to the  memory block allocated for the specified interface.

## -see-also

<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_free">WinUSB_Free</a>