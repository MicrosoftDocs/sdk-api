---
UID: NF:winusb.WinUsb_GetPowerPolicy
title: WinUsb_GetPowerPolicy function
author: windows-sdk-content
description: The WinUsb_GetPowerPolicy function retrieves the power policy for a device. This is a synchronous operation.
old-location: buses\winusb_getpowerpolicy.htm
tech.root: UsbRef
ms.assetid: 515a4548-d89f-458d-89ed-1cc4d25561ef
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WinUsb_GetPowerPolicy, WinUsb_GetPowerPolicy function [Buses], buses.winusb_getpowerpolicy, winusb/WinUsb_GetPowerPolicy, winusbfunc_85084f46-4707-4fd1-8246-61cd4a18eec0.xml
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
 - WinUsb_GetPowerPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinUsb_GetPowerPolicy function


## -description


The <b>WinUsb_GetPowerPolicy</b> function retrieves the power policy for a device. This is a synchronous operation.


## -parameters




### -param InterfaceHandle [in]

An opaque handle to the first interface on the device, which is returned by <a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>. 


### -param PolicyType [in]

A value that specifies the power policy parameter to retrieve in <i>Value</i>. The following table describes symbolic constants that are defined in <i>Winusbio.h</i>. 

<table>
<tr>
<th>Policy type</th>
<th>Description</th>
</tr>
<tr>
<td>
AUTO_SUSPEND

(0x81)

</td>
<td>
If the caller specifies a power policy of AUTO_SUSPEND, <b>WinUsb_GetPowerPolicy</b> returns the value of the auto suspend policy parameter in the <i>Value</i> parameter.

If <i>Value</i> is <b>TRUE</b> (that is, nonzero), the USB stack suspends the device when no transfers are pending or the only transfers pending are IN transfers on an interrupt or bulk endpoint. 

The value of the <b>DefaultIdleState</b> registry value determines the default value of the auto suspend policy parameter.

The <i>Value</i> parameter must point to a UCHAR variable.  

</td>
</tr>
<tr>
<td>
SUSPEND_DELAY

(0x83)

</td>
<td>
If the caller specifies a power policy of SUSPEND_DELAY, <b>WinUsb_GetPowerPolicy</b> returns the value of the suspend delay policy parameter in <i>Value</i>.

The suspend delay policy parameter specifies the minimum amount of time, in milliseconds, that the WinUSB driver must wait after any transfer before it can suspend the device. 

<i>Value</i> must point to a ULONG variable.  

</td>
</tr>
</table>
 


### -param ValueLength [in, out]

A pointer to the size of the buffer that <i>Value</i>. On output, <i>ValueLength</i> receives the size of the data that was copied into the <i>Value </i>buffer.


### -param Value [out]

A buffer that receives the specified power policy parameter. For more information, see <i>PolicyType</i>.


## -returns



<b>WinUsb_GetPowerPolicy</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this routine returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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



<a href="https://msdn.microsoft.com/4925064b-2676-436d-b455-a68f622c543e">WinUSB Power Management</a>



<a href="https://msdn.microsoft.com/258cf508-036a-4ade-95b2-4b36d1149ffd">WinUsb_Initialize</a>
 

 

