---
UID: NF:winusb.WinUsb_GetPipePolicy
title: WinUsb_GetPipePolicy function
author: windows-sdk-content
description: The WinUsb_GetPipePolicy function retrieves the policy for a specific pipe associated with an endpoint on the device. This is a synchronous operation.
old-location: buses\winusb_getpipepolicy.htm
tech.root: usbref
ms.assetid: adf66b3d-cf63-40f1-837a-d83c353236a3
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: WinUsb_GetPipePolicy, WinUsb_GetPipePolicy function [Buses], buses.winusb_getpipepolicy, winusb/WinUsb_GetPipePolicy, winusbfunc_1f0337bd-6717-4123-914b-daecb090ac89.xml
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
 - winusb.dll
api_name:
 - WinUsb_GetPipePolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WinUsb_GetPipePolicy
: 
---

# WinUsb_GetPipePolicy function


## -description


The <b>WinUsb_GetPipePolicy</b> function retrieves the policy for a specific pipe associated with an endpoint on the device. This is a synchronous operation.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface that contains the endpoint with which the pipe is associated.

To query the pipe associated with the endpoint in the first interface, use the handle returned by <a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/1afc7b2f-4fb6-4ab4-8415-aaee9cd6ee0c">WinUsb_GetAssociatedInterface</a>.


### -param PipeID [in]

An 8-bit value that consists of a 7-bit address and a direction bit. This parameter corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor.


### -param PolicyType [in]

A <b>ULONG</b> variable that specifies the policy parameter to retrieve. The current value for the policy parameter is retrieved the <i>Value</i> parameter. For information about the behavior of the pipe policies, see <a href="https://msdn.microsoft.com/fc7d8916-63ab-45a2-a786-8da8e9f3fe56">WinUSB Functions for Pipe Policy Modification</a>.


### -param ValueLength [in, out]

A pointer to the size, in bytes, of the buffer that <i>Value</i> points to. On output, <i>ValueLength</i> receives the size, in bytes, of the data that was copied into the <i>Value </i>buffer.


### -param Value [out]

A pointer to a buffer that receives the specified pipe policy value.


## -returns



<b>WinUsb_GetPipePolicy</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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



<a href="https://msdn.microsoft.com/fc7d8916-63ab-45a2-a786-8da8e9f3fe56">WinUSB Functions for Pipe Policy Modification</a>



<a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>



<a href="https://msdn.microsoft.com/936e535b-9084-4e3d-908e-0e965f658827">WinUsb_ReadPipe</a>



<a href="https://msdn.microsoft.com/995b1d1b-8c08-4e67-8ba5-155231fe37f4">WinUsb_WritePipe</a>
 

 

