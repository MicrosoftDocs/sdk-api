---
UID: NF:winusb.WinUsb_SetPowerPolicy
title: WinUsb_SetPowerPolicy function (winusb.h)
description: The WinUsb_SetPowerPolicy function sets the power policy for a device.
helpviewer_keywords: ["WinUsb_SetPowerPolicy","WinUsb_SetPowerPolicy function [Buses]","buses.winusb_setpowerpolicy","winusb/WinUsb_SetPowerPolicy","winusbfunc_f957d4a1-0ba3-4e43-bf77-74314a5fae59.xml"]
old-location: buses\winusb_setpowerpolicy.htm
tech.root: buses
ms.assetid: 11e56a77-1a9f-418a-94cf-df686d3d7868
ms.date: 12/05/2018
ms.keywords: WinUsb_SetPowerPolicy, WinUsb_SetPowerPolicy function [Buses], buses.winusb_setpowerpolicy, winusb/WinUsb_SetPowerPolicy, winusbfunc_f957d4a1-0ba3-4e43-bf77-74314a5fae59.xml
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
 - WinUsb_SetPowerPolicy
 - winusb/WinUsb_SetPowerPolicy
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
 - WinUsb_SetPowerPolicy
---

# WinUsb_SetPowerPolicy function


## -description

The <b>WinUsb_SetPowerPolicy</b> function sets the power policy for a device.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to the first (default) interface on the device, which is returned by <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>.

### -param PolicyType [in]

A value that specifies the power policy to set. The following table describes symbolic constants that are defined in winusbio.h. 

<table>
<tr>
<th>Policy parameter</th>
<th>Description</th>
</tr>
<tr>
<td>
AUTO_SUSPEND

(0x81)

</td>
<td>
Specifies the auto-suspend policy type; the power policy parameter must be specified by the caller in the <i>Value</i> parameter.

For auto-suspend, the <i>Value</i> parameter must point to a UCHAR variable.  

If <i>Value</i> is <b>TRUE</b> (nonzero), the USB stack suspends the device if the device is idle.  A device is idle if there are no transfers pending, or if the only pending transfers are IN transfers to interrupt or bulk endpoints.  

The default value is determined by the value set in the <b>DefaultIdleState</b> registry setting. By default, this value is <b>TRUE</b>. 

</td>
</tr>
<tr>
<td>
SUSPEND_DELAY

(0x83)

</td>
<td>
Specifies the suspend-delay policy type; the power policy parameter must be specified by the caller in the <i>Value</i> parameter.

For suspend-delay, <i>Value</i> must point to a ULONG variable.  

<i>Value</i> specifies the minimum amount of time, in milliseconds, that the WinUSB driver must wait post transfer before it can suspend the device. 

The default value is determined by the value set in the <b>DefaultIdleTimeout</b> registry setting. By default, this value is five seconds.

</td>
</tr>
</table>

### -param ValueLength [in]

The size, in bytes, of the buffer at <i>Value</i>.

### -param Value [in]

The new value for the power policy parameter. Datatype and value for <i>Value</i> depends on the type of power policy passed in <i>PolicyType</i>. For more information, see <i>PolicyType</i>.

## -returns

<b>WinUsb_SetPowerPolicy</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, this function returns <b>FALSE</b>, and the caller can retrieve the logged error by calling <b>GetLastError</b>.


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

## -remarks

The following list summarizes the effects of changes to power management states:

<ul>
<li>
All pipe handles, interface handles, locks, and alternate settings are preserved across power management events.

</li>
<li>
Any transfers that are in progress are suspended when a device transfers to a low power state, and they are resumed when the device is restored to a working state.

</li>
<li>
The device and system must be in a working state before the client can restore a device-specific configuration. Clients can determine whether the device and system are in a working state from the WM_POWERBROADCAST message.

</li>
<li>
The client can indicate that an interface is idle by calling <b>WinUsb_SetPowerPolicy</b>. 

</li>
</ul>

## -see-also

<a href="/windows-hardware/drivers/ddi/content/index">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows-hardware/drivers/ddi/content/index">WinUSB Power Management</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>