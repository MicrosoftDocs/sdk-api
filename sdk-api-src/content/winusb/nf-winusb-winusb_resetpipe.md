---
UID: NF:winusb.WinUsb_ResetPipe
title: WinUsb_ResetPipe function
author: windows-sdk-content
description: The WinUsb_ResetPipe function resets the data toggle and clears the stall condition on a pipe.
old-location: buses\winusb_resetpipe.htm
tech.root: UsbRef
ms.assetid: 0fd30723-8cb9-4e29-942b-abe48c691d8e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: WinUsb_ResetPipe, WinUsb_ResetPipe function [Buses], buses.winusb_resetpipe, winusb/WinUsb_ResetPipe, winusbfunc_6d4baf88-4b6f-46fb-802b-67ac51ddaf8d.xml
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WinUsb_ResetPipe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinUsb_ResetPipe function


## -description


The <b>WinUsb_ResetPipe</b> function resets the data toggle and clears the stall condition on a pipe.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to the interface that contains the endpoint with which the pipe is associated. 

To reset a pipe associated with an endpoint in the first interface, use the handle returned by <a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/1afc7b2f-4fb6-4ab4-8415-aaee9cd6ee0c">WinUsb_GetAssociatedInterface</a>.


### -param PipeID [in]

The identifier (ID) of the control pipe. The <i>PipeID</i> parameter is an 8-bit value that consists in a 7-bit address and a direction bit. This parameter corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor.


## -returns



<b>WinUsb_ResetPipe</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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



<a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>
 

 

