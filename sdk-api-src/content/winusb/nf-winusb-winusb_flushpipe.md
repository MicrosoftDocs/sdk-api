---
UID: NF:winusb.WinUsb_FlushPipe
title: WinUsb_FlushPipe function
author: windows-sdk-content
description: The WinUsb_FlushPipe function discards any data that is cached in a pipe. This is a synchronous operation.
old-location: buses\winusb_flushpipe.htm
old-project: usbref
ms.assetid: 3f6d55c2-32df-4cb9-99bb-0e1a71c97394
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WinUsb_FlushPipe, WinUsb_FlushPipe function [Buses], buses.winusb_flushpipe, winusb/WinUsb_FlushPipe, winusbfunc_44ebf8ef-770d-4102-8a2d-b0d996f36e41.xml
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
 - WinUsb_FlushPipe
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_FlushPipe function


## -description


The <b>WinUsb_FlushPipe</b> function discards any data that is cached in a pipe. This is a synchronous operation.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to the interface with which the specified pipe's endpoint is associated. To clear data in a pipe that is associated with the endpoint on the first (default) interface, use the handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540245">WinUsb_GetAssociatedInterface</a>.


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




<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>
 

 

