---
UID: NF:winusb.WinUsb_SetPipePolicy
title: WinUsb_SetPipePolicy function
author: windows-sdk-content
description: The WinUsb_SetPipePolicy function sets the policy for a specific pipe associated with an endpoint on the device. This is a synchronous operation.
old-location: buses\winusb_setpipepolicy.htm
old-project: usbref
ms.assetid: 34bd7798-4c5f-48c9-bcd1-1492693b0639
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: WinUsb_SetPipePolicy, WinUsb_SetPipePolicy function [Buses], buses.winusb_setpipepolicy, winusb/WinUsb_SetPipePolicy, winusbfunc_8a973602-4564-42df-9adf-b7ea6a0339e9.xml
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
 - winusb.dll
api_name:
 - WinUsb_SetPipePolicy
product: Windows
targetos: Windows
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WinUsb_SetPipePolicy function


## -description


The <b>WinUsb_SetPipePolicy</b> function sets the policy for a specific pipe associated with an endpoint on the device. This is a synchronous operation.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to an interface that contains the endpoint with which the pipe is associated. 

To set policy for the pipe associated with the endpoint in the first interface, use the handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540245">WinUsb_GetAssociatedInterface</a>.


### -param PipeID [in]

An 8-bit value that consists of a 7-bit address and a direction bit. This parameter corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor.


### -param PolicyType [in]

A <b>ULONG</b> variable that specifies the policy parameter to change. The <i>Value</i> parameter contains the new value for the policy parameter, defined in <i>winusbio.h</i>. For information about how to use each of the pipe policies and the resulting behavior, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff728833">WinUSB Functions for Pipe Policy Modification</a>. 


### -param ValueLength [in]

The size, in bytes, of the buffer at <i>Value</i>.


### -param Value [in]

The new value for the policy parameter that <i>PolicyType</i> specifies. The size of this input parameter depends on the policy to change. For information about the size of this parameter, see the description of the <i>PolicyType</i> parameter.


## -returns



<b>WinUsb_SetPipePolicy</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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
The caller passed an invalid size for the policy parameter buffer in the <i>ValueLength</i> parameter.

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
 




## -see-also




<a href="https://msdn.microsoft.com/8234d0b4-2c73-45fa-a8bf-566c64cc2858">WinUSB</a>



<a href="https://docs.microsoft.com/en-us/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff728833">WinUSB Functions for Pipe Policy Modification</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540266">WinUsb_GetPipePolicy</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540277">WinUsb_Initialize</a>
 

 

