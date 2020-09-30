---
UID: NF:winusb.WinUsb_ControlTransfer
title: WinUsb_ControlTransfer function (winusb.h)
description: The WinUsb_ControlTransfer function transmits control data over a default control endpoint.
helpviewer_keywords: ["WinUsb_ControlTransfer","WinUsb_ControlTransfer function [Buses]","buses.winusb_controltransfer","winusb/WinUsb_ControlTransfer","winusbfunc_016c7bb1-6139-4a37-95d9-f3e2312871a2.xml"]
old-location: buses\winusb_controltransfer.htm
tech.root: buses
ms.assetid: 2ae80c97-3a09-4e90-ae73-92b5caa5cf99
ms.date: 12/05/2018
ms.keywords: WinUsb_ControlTransfer, WinUsb_ControlTransfer function [Buses], buses.winusb_controltransfer, winusb/WinUsb_ControlTransfer, winusbfunc_016c7bb1-6139-4a37-95d9-f3e2312871a2.xml
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
 - WinUsb_ControlTransfer
 - winusb/WinUsb_ControlTransfer
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
 - WinUsb_ControlTransfer
---

# WinUsb_ControlTransfer function


## -description

The <b>WinUsb_ControlTransfer</b> function transmits control data over a default control endpoint.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. 

To specify the recipient of  a control request as the entire device or the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, obtain the handle to the target interface by calling <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>, and then call <b>WinUsb_ControlTransfer</b> by specifying the obtained interface handle.

### -param SetupPacket [in]

The 8-byte setup packet of type <a href="/windows/desktop/api/winusb/ns-winusb-winusb_setup_packet">WINUSB_SETUP_PACKET</a>.

### -param Buffer [out]

A caller-allocated buffer that contains the data to transfer. The length of this buffer must not exceed 4KB.

### -param BufferLength [in]

The number of bytes to transfer, not including the setup packet. This number must be less than or equal to the size, in bytes, of <i>Buffer</i>.

### -param LengthTransferred [out, optional]

A pointer to a ULONG variable that receives the actual number of transferred bytes. If the application does not expect any data to be transferred during the
        data phase (<i>BufferLength</i> is zero),  <i>LengthTransferred</i> can be <b>NULL</b>.

### -param Overlapped [in, optional]

An optional pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, which is used for asynchronous operations. If this parameter is specified, <b>WinUsb_ControlTransfer</b> immediately returns, and the event is signaled when the operation is complete. If <i>Overlapped</i> is not supplied, the <b>WinUsb_ControlTransfer</b> function transfers data synchronously.

## -returns

<b>WinUsb_ControlTransfer</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
The caller passed <b>NULL</b> in the  <i>InterfaceHandle</i> parameter.

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
</table>

## -remarks

A control request is always sent by the host to the default endpoint of a USB device but the recipient of the request can be the entire device, an interface, or an endpoint in the selected alternate setting. In the <b>WinUsb_ControlTransfer</b> call, the application must indicate the recipient through two parameters: <i>InterfaceHandle</i> and <i>SetupPacket</i>. 

If the recipient of a control request is the entire device, the first interface, or any endpoint in that interface, the application must use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. If the recipient is any other interface or its endpoint, then the application must obtain the WinUSB handle that is associated with the target interface by calling <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>, and then call <b>WinUsb_ControlTransfer</b> by specifying the obtained interface handle.

As per Section 9.3 of the official USB specification, the setup token of a control transfer contains information about the request. For a WinUSB application, that setup token is described by using the <a href="/windows/desktop/api/winusb/ns-winusb-winusb_setup_packet">WINUSB_SETUP_PACKET</a> structure. 

Within the setup token, <b>bmRequestType</b> and <b>wIndex</b> fields are used to indicate the recipient of the request. Those fields correspond to <b>RequestType</b> and <b>Index</b> members of <a href="/windows/desktop/api/winusb/ns-winusb-winusb_setup_packet">WINUSB_SETUP_PACKET</a>, respectively. 

The lowest two bits of <b>RequestType</b> indicate the recipient of the request. The recipient can be the device, an interface, endpoint, or other (for vendor request). Depending on the recipient, the lower byte of <b>Index</b> indicates the device-defined index of the recipient. The value of <b>Index</b> depends on the type of request. For example, for standard control requests, the value is 0, or indicates the interface or endpoint number. For certain types of standard requests, such as a GET_DESCRIPTOR request to obtain a string descriptor, the <b>Index</b> value indicates the Language ID. 

If the recipient is the device, the application must set <b>RequestType</b> and <b>Index</b> values.  The lowest two bits of <b>RequestType</b> value must be 0. The lower byte of <b>Index</b> value depends on the type of request. The <i>InterfaceHandle</i> must be the WinUSB handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

If the recipient of the request is an interface, the application must set the lowest two bits of <b>RequestType</b> to 0x01. The application is not required to set the lower byte of <b>Index</b> for any type of request. For  standard, class, and vendor requests,  Winusb.sys sets the value to the interface number of the target interface. The <i>InterfaceHandle</i> must be associated with the target interface. The application can obtain that handle by calling <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

If the recipient is an endpoint, the application must set the lowest two bits of <b>RequestType</b> to 0x02 and lower byte of Index to the endpoint address. In this case, <i>InterfaceHandle</i> is associated with the interface that contains the endpoint. The application can obtain that handle by calling <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

## -see-also

<a href="/windows/desktop/api/winusb/ns-winusb-winusb_setup_packet">WINUSB_SETUP_PACKET</a>



<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>