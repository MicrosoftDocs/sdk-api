---
UID: NF:powrprof.DevicePowerEnumDevices
title: DevicePowerEnumDevices function (powrprof.h)
description: Enumerates devices on the system that meet the specified criteria.
helpviewer_keywords: ["DEVICEPOWER_AND_OPERATION","DEVICEPOWER_FILTER_DEVICES_PRESENT","DEVICEPOWER_FILTER_ON_NAME","DEVICEPOWER_FILTER_WAKEENABLED","DEVICEPOWER_HARDWAREID","DevicePowerEnumDevices","DevicePowerEnumDevices function","PDCAP_D0_SUPPORTED","PDCAP_D1_SUPPORTED","PDCAP_D2_SUPPORTED","PDCAP_D3_SUPPORTED","PDCAP_S0_SUPPORTED","PDCAP_S1_SUPPORTED","PDCAP_S2_SUPPORTED","PDCAP_S3_SUPPORTED","PDCAP_S4_SUPPORTED","PDCAP_S5_SUPPORTED","PDCAP_WAKE_FROM_D0_SUPPORTED","PDCAP_WAKE_FROM_D1_SUPPORTED","PDCAP_WAKE_FROM_D2_SUPPORTED","PDCAP_WAKE_FROM_D3_SUPPORTED","PDCAP_WAKE_FROM_S0_SUPPORTED","PDCAP_WAKE_FROM_S1_SUPPORTED","PDCAP_WAKE_FROM_S2_SUPPORTED","PDCAP_WAKE_FROM_S3_SUPPORTED","PDCAP_WARM_EJECT_SUPPORTED","base.devicepowerenumdevices","powrprof/DevicePowerEnumDevices"]
old-location: base\devicepowerenumdevices.htm
tech.root: base
ms.assetid: bb67634c-69d9-4194-ac27-4f9740d73a1a
ms.date: 12/05/2018
ms.keywords: DEVICEPOWER_AND_OPERATION, DEVICEPOWER_FILTER_DEVICES_PRESENT, DEVICEPOWER_FILTER_ON_NAME, DEVICEPOWER_FILTER_WAKEENABLED, DEVICEPOWER_HARDWAREID, DevicePowerEnumDevices, DevicePowerEnumDevices function, PDCAP_D0_SUPPORTED, PDCAP_D1_SUPPORTED, PDCAP_D2_SUPPORTED, PDCAP_D3_SUPPORTED, PDCAP_S0_SUPPORTED, PDCAP_S1_SUPPORTED, PDCAP_S2_SUPPORTED, PDCAP_S3_SUPPORTED, PDCAP_S4_SUPPORTED, PDCAP_S5_SUPPORTED, PDCAP_WAKE_FROM_D0_SUPPORTED, PDCAP_WAKE_FROM_D1_SUPPORTED, PDCAP_WAKE_FROM_D2_SUPPORTED, PDCAP_WAKE_FROM_D3_SUPPORTED, PDCAP_WAKE_FROM_S0_SUPPORTED, PDCAP_WAKE_FROM_S1_SUPPORTED, PDCAP_WAKE_FROM_S2_SUPPORTED, PDCAP_WAKE_FROM_S3_SUPPORTED, PDCAP_WARM_EJECT_SUPPORTED, base.devicepowerenumdevices, powrprof/DevicePowerEnumDevices
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
 - DevicePowerEnumDevices
 - powrprof/DevicePowerEnumDevices
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
 - DevicePowerEnumDevices
---

# DevicePowerEnumDevices function


## -description

Enumerates devices on the system that meet the specified criteria.

## -parameters

### -param QueryIndex [in]

The index of the requested device. For initial calls, this value should be zero.

### -param QueryInterpretationFlags [in]

The criteria applied to the search results.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_HARDWAREID"></a><a id="devicepower_hardwareid"></a><dl>
<dt><b>DEVICEPOWER_HARDWAREID</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Return a hardware ID string rather than friendly device name.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_FILTER_DEVICES_PRESENT"></a><a id="devicepower_filter_devices_present"></a><dl>
<dt><b>DEVICEPOWER_FILTER_DEVICES_PRESENT</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Ignore devices not currently present in the system.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_AND_OPERATION"></a><a id="devicepower_and_operation"></a><dl>
<dt><b>DEVICEPOWER_AND_OPERATION</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Perform an AND operation on <i>QueryFlags</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_FILTER_WAKEENABLED"></a><a id="devicepower_filter_wakeenabled"></a><dl>
<dt><b>DEVICEPOWER_FILTER_WAKEENABLED</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Check whether the device is currently enabled to wake the system from a sleep state.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_FILTER_ON_NAME"></a><a id="devicepower_filter_on_name"></a><dl>
<dt><b>DEVICEPOWER_FILTER_ON_NAME</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
Find a device whose name matches the string passed in <i>pReturnBuffer</i> and check 
        its capabilities against <i>QueryFlags</i>.

</td>
</tr>
</table>

### -param QueryFlags [in]

The query criteria.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDCAP_D0_SUPPORTED"></a><a id="pdcap_d0_supported"></a><dl>
<dt><b>PDCAP_D0_SUPPORTED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The device supports system power state D0.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_D1_SUPPORTED"></a><a id="pdcap_d1_supported"></a><dl>
<dt><b>PDCAP_D1_SUPPORTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The device supports system power state D1.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_D2_SUPPORTED"></a><a id="pdcap_d2_supported"></a><dl>
<dt><b>PDCAP_D2_SUPPORTED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The device supports system power state D2.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_D3_SUPPORTED"></a><a id="pdcap_d3_supported"></a><dl>
<dt><b>PDCAP_D3_SUPPORTED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The device supports system power state D3.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_S0_SUPPORTED"></a><a id="pdcap_s0_supported"></a><dl>
<dt><b>PDCAP_S0_SUPPORTED</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The device supports system sleep state S0.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_S1_SUPPORTED"></a><a id="pdcap_s1_supported"></a><dl>
<dt><b>PDCAP_S1_SUPPORTED</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The device supports system sleep state S1.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_S2_SUPPORTED"></a><a id="pdcap_s2_supported"></a><dl>
<dt><b>PDCAP_S2_SUPPORTED</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The device supports system sleep state S2.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_S3_SUPPORTED"></a><a id="pdcap_s3_supported"></a><dl>
<dt><b>PDCAP_S3_SUPPORTED</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The device supports system sleep state S3.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_S4_SUPPORTED"></a><a id="pdcap_s4_supported"></a><dl>
<dt><b>PDCAP_S4_SUPPORTED</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The device supports system sleep state S4.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_S5_SUPPORTED"></a><a id="pdcap_s5_supported"></a><dl>
<dt><b>PDCAP_S5_SUPPORTED</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The device supports system sleep state S5.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_D0_SUPPORTED"></a><a id="pdcap_wake_from_d0_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_D0_SUPPORTED</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system power state D0.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_D1_SUPPORTED"></a><a id="pdcap_wake_from_d1_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_D1_SUPPORTED</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system power state D1.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_D2_SUPPORTED"></a><a id="pdcap_wake_from_d2_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_D2_SUPPORTED</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system power state D2.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_D3_SUPPORTED"></a><a id="pdcap_wake_from_d3_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_D3_SUPPORTED</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system power state D3.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_S0_SUPPORTED"></a><a id="pdcap_wake_from_s0_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_S0_SUPPORTED</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system sleep state S0.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_S1_SUPPORTED"></a><a id="pdcap_wake_from_s1_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_S1_SUPPORTED</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system sleep state S1.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_S2_SUPPORTED"></a><a id="pdcap_wake_from_s2_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_S2_SUPPORTED</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system sleep state S2.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WAKE_FROM_S3_SUPPORTED"></a><a id="pdcap_wake_from_s3_supported"></a><dl>
<dt><b>PDCAP_WAKE_FROM_S3_SUPPORTED</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
The device supports waking from system sleep state S3.

</td>
</tr>
<tr>
<td width="40%"><a id="PDCAP_WARM_EJECT_SUPPORTED"></a><a id="pdcap_warm_eject_supported"></a><dl>
<dt><b>PDCAP_WARM_EJECT_SUPPORTED</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The device supports warm eject.

</td>
</tr>
</table>

### -param pReturnBuffer [out, optional]

Pointer to a buffer that receives the requested information.

### -param pBufferSize [in, out]

The size, in bytes, of the return buffer.
      

<div class="alert"><b>Note</b>  If <i>pReturnBuffer</i> is <b>NULL</b>, 
       <i>pBufferSize</i> will be filled with the size needed to return the data.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The values of the <i>QueryFlags</i> parameter may be combined to query for devices that 
     support two or more criteria. For example; if <b>PDCAP_D3_SUPPORTED</b> | 
     <b>PDCAP_D1_SUPPORTED</b> is passed as the <i>QueryFlags</i> parameter, the 
     function will query for devices that support either D3 or D1.

<i>QueryFlags</i> also may be combined with 
     <i>QueryInterpretationFlags</i> set to <b>DEVICEPOWER_AND_OPERATION</b> to 
     produce a query of devices that support all of the requested criteria. For example; if 
     <b>PDCAP_D3_SUPPORTED</b> | <b>PDCAP_D1_SUPPORTED</b> is passed as the 
     <i>QueryFlags</i> parameter and <b>DEVICEPOWER_AND_OPERATION</b> is passed 
     as the <i>QueryInterpretationFlags</i> parameter, the function will query devices that support 
     both D3 and D1.


#### Examples

For an example that uses this function, see 
     <a href="/windows/desktop/Power/using-the-device-power-api">Using the Device Power API</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Power/device-power-management">Device Power Management</a>