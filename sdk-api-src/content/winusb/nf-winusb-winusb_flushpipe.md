---
UID: NF:winusb.WinUsb_FlushPipe
title: WinUsb_FlushPipe function (winusb.h)
description: The WinUsb_FlushPipe function discards any data that is cached in a pipe. This is a synchronous operation.
helpviewer_keywords: ["WinUsb_FlushPipe","WinUsb_FlushPipe function [Buses]","buses.winusb_flushpipe","winusb/WinUsb_FlushPipe","winusbfunc_44ebf8ef-770d-4102-8a2d-b0d996f36e41.xml"]
old-location: buses\winusb_flushpipe.htm
tech.root: buses
ms.assetid: 3f6d55c2-32df-4cb9-99bb-0e1a71c97394
ms.date: 12/05/2018
ms.keywords: WinUsb_FlushPipe, WinUsb_FlushPipe function [Buses], buses.winusb_flushpipe, winusb/WinUsb_FlushPipe, winusbfunc_44ebf8ef-770d-4102-8a2d-b0d996f36e41.xml
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
 - WinUsb_FlushPipe
 - winusb/WinUsb_FlushPipe
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
 - WinUsb_FlushPipe
---

# WinUsb_FlushPipe function


## -description

The <b>WinUsb_FlushPipe</b> function discards any data that is cached in a pipe. This is a synchronous operation.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to the interface with which the specified pipe's endpoint is associated. To clear data in a pipe that is associated with the endpoint on the first (default) interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param PipeID [in]

The identifier (ID) of the control pipe. The <i>PipeID</i> parameter is an 8-bit value that consists of a 7-bit address and a direction bit. This parameter corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor.

## -returns

<b>WinUsb_FlushPipe</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>