---
UID: NF:winusb.WinUsb_GetAssociatedInterface
title: WinUsb_GetAssociatedInterface function
author: windows-sdk-content
description: The WinUsb_GetAssociatedInterface function retrieves a handle for an associated interface. This is a synchronous operation.
old-location: buses\winusb_getassociatedinterface.htm
old-project: usbref
ms.assetid: 1afc7b2f-4fb6-4ab4-8415-aaee9cd6ee0c
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: WinUsb_GetAssociatedInterface, WinUsb_GetAssociatedInterface function [Buses], buses.winusb_getassociatedinterface, winusb/WinUsb_GetAssociatedInterface, winusbfunc_22b6f592-12ca-433e-b7a1-885eebf60386.xml
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WIN_CERTIFICATE, *LPWIN_CERTIFICATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_GetAssociatedInterface
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_GetAssociatedInterface function


## -description


The <b>WinUsb_GetAssociatedInterface</b> function retrieves a handle for an associated interface. This is a synchronous operation.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to the first (default) interface on the device, which is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>. 


### -param AssociatedInterfaceIndex [in]

An index that specifies the associated interface to retrieve. A value of 0 indicates the first associated interface, a value of 1 indicates the second associated interface, and so on.


### -param AssociatedInterfaceHandle [out]

A handle for the associated interface. Callers must pass this interface handle to <a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a> exposed by Winusb.dll. To close this handle, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540233">WinUsb_Free</a>.


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

<a href="https://msdn.microsoft.com/library/windows/hardware/ff540245">WinUsb_GetAssociatedInterface</a> has already returned a handle for the interface that <i>AssociatedInterfaceIndex</i> specifies.

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

The <i>first associated interface</i> is the interface that immediately follows the interface whose handle the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a> routine retrieves.

The handle that <b>WinUsb_GetAssociatedInterface</b> returns must be released by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff540233">WinUsb_Free</a>.

Callers of <b>WinUsb_GetAssociatedInterface</b>can retrieve only one handle for each interface. If a caller attempts to retrieve more than one handle for the same interface, the routine will fail with an error of ERROR_ALREADY_EXISTS.




## -see-also




<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>
 

 

