---
UID: NF:winusb.WinUsb_AbortPipe
title: WinUsb_AbortPipe function (winusb.h)
description: The WinUsb_AbortPipe function aborts all of the pending transfers for a pipe. This is a synchronous operation.
helpviewer_keywords: ["WinUsb_AbortPipe","WinUsb_AbortPipe function [Buses]","buses.winusb_abortpipe","winusb/WinUsb_AbortPipe","winusbfunc_2cd765f4-18f0-462e-a6e1-c86f00232035.xml"]
old-location: buses\winusb_abortpipe.htm
tech.root: buses
ms.assetid: 08695612-d579-41e4-a8b6-1de44a57aeaa
ms.date: 12/05/2018
ms.keywords: WinUsb_AbortPipe, WinUsb_AbortPipe function [Buses], buses.winusb_abortpipe, winusb/WinUsb_AbortPipe, winusbfunc_2cd765f4-18f0-462e-a6e1-c86f00232035.xml
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
 - WinUsb_AbortPipe
 - winusb/WinUsb_AbortPipe
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
 - WinUsb_AbortPipe
---

# WinUsb_AbortPipe function


## -description

The <b>WinUsb_AbortPipe</b> function aborts all of the pending transfers for a pipe. This is a synchronous operation.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface that contains the endpoint with which the pipe is associated.

To abort transfers on the pipe associated with the endpoint in the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param PipeID [in]

The identifier (ID) of the control pipe. The <i>PipeID</i> parameter is an 8-bit value that consists of a 7-bit address and a direction bit. This parameter corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor.

## -returns

<b>WinUsb_AbortPipe</b> returns <b>TRUE</b> if  the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>. 


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

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_free">WinUsb_Free</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>