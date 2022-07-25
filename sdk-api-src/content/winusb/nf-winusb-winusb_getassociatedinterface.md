---
UID: NF:winusb.WinUsb_GetAssociatedInterface
title: WinUsb_GetAssociatedInterface function (winusb.h)
description: The WinUsb_GetAssociatedInterface function retrieves a handle for an associated interface. This is a synchronous operation.
helpviewer_keywords: ["WinUsb_GetAssociatedInterface","WinUsb_GetAssociatedInterface function [Buses]","buses.winusb_getassociatedinterface","winusb/WinUsb_GetAssociatedInterface","winusbfunc_22b6f592-12ca-433e-b7a1-885eebf60386.xml"]
old-location: buses\winusb_getassociatedinterface.htm
tech.root: buses
ms.assetid: 1afc7b2f-4fb6-4ab4-8415-aaee9cd6ee0c
ms.date: 12/05/2018
ms.keywords: WinUsb_GetAssociatedInterface, WinUsb_GetAssociatedInterface function [Buses], buses.winusb_getassociatedinterface, winusb/WinUsb_GetAssociatedInterface, winusbfunc_22b6f592-12ca-433e-b7a1-885eebf60386.xml
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
 - WinUsb_GetAssociatedInterface
 - winusb/WinUsb_GetAssociatedInterface
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
 - WinUsb_GetAssociatedInterface
---

# WinUsb_GetAssociatedInterface function


## -description

The <b>WinUsb_GetAssociatedInterface</b> function retrieves a handle for an associated interface. This is a synchronous operation.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to the first (default) interface on the device, which is returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

### -param AssociatedInterfaceIndex [in]

An index that specifies the associated interface to retrieve. A value of 0 indicates the first associated interface, a value of 1 indicates the second associated interface, and so on.

### -param AssociatedInterfaceHandle [out]

A handle for the associated interface. Callers must pass this interface handle to <a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a> exposed by Winusb.dll. To close this handle, call <a href="/windows/desktop/api/winusb/nf-winusb-winusb_free">WinUsb_Free</a>.

## -returns

<b>WinUsb_GetAssociatedInterface</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a> has already returned a handle for the interface that <i>AssociatedInterfaceIndex</i> specifies.

</td>
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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
 The passed <i>AssociatedInterfaceIndex</i> value failed an integer overflow check. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
An interface does not exist for the specified <i>AssociatedInterfaceIndex</i> value<i>.</i>

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

The <b>WinUsb_GetAssociatedInterface</b> routine retrieves an opaque handle.

The <i>first associated interface</i> is the interface that immediately follows the interface whose handle the <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a> routine retrieves.

The handle that <b>WinUsb_GetAssociatedInterface</b> returns must be released by calling <a href="/windows/desktop/api/winusb/nf-winusb-winusb_free">WinUsb_Free</a>.

Callers of <b>WinUsb_GetAssociatedInterface</b> can retrieve only one handle for each interface. If a caller attempts to retrieve more than one handle for the same interface, the routine will fail with an error of ERROR_ALREADY_EXISTS.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>