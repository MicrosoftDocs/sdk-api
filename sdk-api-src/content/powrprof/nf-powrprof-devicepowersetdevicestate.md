---
UID: NF:powrprof.DevicePowerSetDeviceState
title: DevicePowerSetDeviceState function (powrprof.h)
description: Modifies the specified data on the specified device.
helpviewer_keywords: ["DEVICEPOWER_CLEAR_WAKEENABLED","DEVICEPOWER_SET_WAKEENABLED","DevicePowerSetDeviceState","DevicePowerSetDeviceState function","base.devicepowersetdevicestate","powrprof/DevicePowerSetDeviceState"]
old-location: base\devicepowersetdevicestate.htm
tech.root: base
ms.assetid: 300842ae-d7d4-42c2-959c-e1713f466d32
ms.date: 12/05/2018
ms.keywords: DEVICEPOWER_CLEAR_WAKEENABLED, DEVICEPOWER_SET_WAKEENABLED, DevicePowerSetDeviceState, DevicePowerSetDeviceState function, base.devicepowersetdevicestate, powrprof/DevicePowerSetDeviceState
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DevicePowerSetDeviceState
 - powrprof/DevicePowerSetDeviceState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - DevicePowerSetDeviceState
---

# DevicePowerSetDeviceState function


## -description

Modifies the specified data on the specified device.

## -parameters

### -param DeviceDescription [in]

The name or hardware identifier string of the device to be modified.

### -param SetFlags [in]

The properties of the device that are to be modified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_SET_WAKEENABLED"></a><a id="devicepower_set_wakeenabled"></a><dl>
<dt><b>DEVICEPOWER_SET_WAKEENABLED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables the specified device to wake the system.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_CLEAR_WAKEENABLED"></a><a id="devicepower_clear_wakeenabled"></a><dl>
<dt><b>DEVICEPOWER_CLEAR_WAKEENABLED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Stops the specified device from being able to wake the system.

</td>
</tr>
</table>

### -param SetData [in]

Reserved, must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
	      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/Power/device-power-management">Device Power Management</a>