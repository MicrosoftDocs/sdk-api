---
UID: NF:winusb.WinUsb_QueryPipeEx
title: WinUsb_QueryPipeEx function
author: windows-sdk-content
description: The WinUsb_QueryPipeEx function retrieves extended information about the specified endpoint and the associated pipe for an interface.
old-location: buses\winusb_querypipeex.htm
tech.root: usbref
ms.assetid: 73C291EC-2345-454B-BC7C-8A443DDFF57C
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: WinUsb_QueryPipeEx, WinUsb_QueryPipeEx function [Buses], buses.winusb_querypipeex, winusb/WinUsb_QueryPipeEx
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
 - WinUsb_QueryPipeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinUsb_QueryPipeEx function


## -description


The <b>WinUsb_QueryPipeEx</b> function retrieves extended information about the specified endpoint and the associated pipe for an interface.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface that contains the endpoint with which the pipe is associated.

To query the pipe associated with an endpoint in the first interface, use the handle returned by <a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/1afc7b2f-4fb6-4ab4-8415-aaee9cd6ee0c">WinUsb_GetAssociatedInterface</a>.


### -param AlternateSettingNumber [in]

A value that specifies the alternate interface to return the information for.


### -param PipeIndex [in]

A value that specifies the pipe to return information about. This value is not the same as the <b>bEndpointAddress</b> field in the endpoint descriptor. A <i>PipeIndex </i>value of 0 signifies the first endpoint that is associated with the interface, a value of 1 signifies the second endpoint, and so on. <i>PipeIndex</i> must be less than the value in the <b>bNumEndpoints</b> field of the interface descriptor.


### -param PipeInformationEx [out]

A pointer, on output, to a caller-allocated <a href="https://msdn.microsoft.com/1A70E67D-8A1E-4041-A1E4-E322317E2849">WINUSB_PIPE_INFORMATION_EX</a> structure that contains pipe information.


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




<a href="https://msdn.microsoft.com/E850ACF2-7FF7-42A2-B3FA-3CFE3A3968E3">Send USB isochronous transfers from a WinUSB desktop app</a>



<a href="https://msdn.microsoft.com/59e1d5e3-8c42-4f2f-b9a4-c637206d5494">WINUSB_PIPE_INFORMATION</a>



<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>
 

 

