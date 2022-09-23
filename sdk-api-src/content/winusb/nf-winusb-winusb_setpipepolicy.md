---
UID: NF:winusb.WinUsb_SetPipePolicy
title: WinUsb_SetPipePolicy function (winusb.h)
description: The WinUsb_SetPipePolicy function sets the policy for a specific pipe associated with an endpoint on the device. This is a synchronous operation.
helpviewer_keywords: ["WinUsb_SetPipePolicy","WinUsb_SetPipePolicy function [Buses]","buses.winusb_setpipepolicy","winusb/WinUsb_SetPipePolicy","winusbfunc_8a973602-4564-42df-9adf-b7ea6a0339e9.xml"]
old-location: buses\winusb_setpipepolicy.htm
tech.root: buses
ms.assetid: 34bd7798-4c5f-48c9-bcd1-1492693b0639
ms.date: 12/05/2018
ms.keywords: WinUsb_SetPipePolicy, WinUsb_SetPipePolicy function [Buses], buses.winusb_setpipepolicy, winusb/WinUsb_SetPipePolicy, winusbfunc_8a973602-4564-42df-9adf-b7ea6a0339e9.xml
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
 - WinUsb_SetPipePolicy
 - winusb/WinUsb_SetPipePolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - winusb.dll
api_name:
 - WinUsb_SetPipePolicy
---

# WinUsb_SetPipePolicy function


## -description

The <b>WinUsb_SetPipePolicy</b> function sets the policy for a specific pipe associated with an endpoint on the device. This is a synchronous operation.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface that contains the endpoint with which the pipe is associated. 

To set policy for the pipe associated with the endpoint in the first interface, use the handle returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>. For all other interfaces, use the handle to the target interface, retrieved by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

### -param PipeID [in]

An 8-bit value that consists of a 7-bit address and a direction bit. This parameter corresponds to the <b>bEndpointAddress</b> field in the endpoint descriptor.

### -param PolicyType [in]

A <b>ULONG</b> variable that specifies the policy parameter to change. The <i>Value</i> parameter contains the new value for the policy parameter, defined in <i>winusbio.h</i>. For information about how to use each of the pipe policies and the resulting behavior, see <a href="[/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification]">WinUSB Functions for Pipe Policy Modification</a>.

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

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows-hardware/drivers/ddi/content/index">WinUSB Functions for Pipe Policy Modification</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_getpipepolicy">WinUsb_GetPipePolicy</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>
