---
UID: NF:winusb.WinUsb_QueryPipeEx
title: WinUsb_QueryPipeEx function (winusb.h)
description: The WinUsb_QueryPipeEx function retrieves extended information about the specified endpoint and the associated pipe for an interface.
helpviewer_keywords: ["WinUsb_QueryPipeEx","WinUsb_QueryPipeEx function [Buses]","buses.winusb_querypipeex","winusb/WinUsb_QueryPipeEx"]
old-location: buses\winusb_querypipeex.htm
tech.root: buses
ms.assetid: 73C291EC-2345-454B-BC7C-8A443DDFF57C
ms.date: 12/05/2018
ms.keywords: WinUsb_QueryPipeEx, WinUsb_QueryPipeEx function [Buses], buses.winusb_querypipeex, winusb/WinUsb_QueryPipeEx
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
 - WinUsb_QueryPipeEx
 - winusb/WinUsb_QueryPipeEx
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
 - WinUsb_QueryPipeEx
---

# WinUsb_QueryPipeEx function


## -description

The <b>WinUsb_QueryPipeEx</b> function retrieves extended information about the specified endpoint and the associated pipe for an interface.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface that contains the endpoint with which the pipe is associated.

To query the pipe associated with an endpoint in the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param AlternateSettingNumber [in]

A value that specifies the alternate interface to return the information for.

### -param PipeIndex [in]

A value that specifies the pipe to return information about. This value is not the same as the <b>bEndpointAddress</b> field in the endpoint descriptor. A <i>PipeIndex </i> value of 0 signifies the first endpoint that is associated with the interface, a value of 1 signifies the second endpoint, and so on. <i>PipeIndex</i> must be less than the value in the <b>bNumEndpoints</b> field of the interface descriptor.

### -param PipeInformationEx [out]

A pointer, on output, to a caller-allocated <a href="/windows/desktop/api/winusbio/ns-winusbio-winusb_pipe_information_ex">WINUSB_PIPE_INFORMATION_EX</a> structure that contains pipe information.

## -returns

<b>WinUsb_QueryPipeEx</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
<dt><b>ERROR_INVALID_PARAMETER </b></dt>
</dl>
</td>
<td width="60%">
The caller passed <b>NULL</b> in the  <i>PipeInformation </i> parameter; interface descriptor could not be found for the handle specified in <i>InterfaceHandle</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>PipeIndex</i> parameter is greater than the  <b>bNumEndpoints</b> value of the interface descriptor; endpoint descriptor could not be found for the specified interface.

</td>
</tr>
</table>

## -remarks

The <b>WinUsb_QueryPipeEx</b> function does not retrieve information about the control pipe.

## -see-also

<a href="/windows-hardware/drivers/usbcon/">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="/windows/desktop/api/winusbio/ns-winusbio-winusb_pipe_information">WINUSB_PIPE_INFORMATION</a>



<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>