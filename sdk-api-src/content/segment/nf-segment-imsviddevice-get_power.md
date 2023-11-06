---
UID: NF:segment.IMSVidDevice.get_Power
title: IMSVidDevice::get_Power (segment.h)
description: The get_Power method queries whether the device is off or on.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get_Power method","IMSVidDevice.get_Power","IMSVidDevice::get_Power","IMSVidDeviceget_Power","get_Power","get_Power method [Microsoft TV Technologies]","get_Power method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get_power","segment/IMSVidDevice::get_Power"]
old-location: mstv\imsviddevice_get_power.htm
tech.root: mstv
ms.assetid: 3be4247b-43d4-4a32-8643-7eb2637aee6f
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Power method, IMSVidDevice.get_Power, IMSVidDevice::get_Power, IMSVidDeviceget_Power, get_Power, get_Power method [Microsoft TV Technologies], get_Power method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_power, segment/IMSVidDevice::get_Power
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidDevice::get_Power
 - segment/IMSVidDevice::get_Power
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidDevice.get_Power
---

# IMSVidDevice::get_Power


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Power</b> method queries whether the device is off or on.

## -parameters

### -param Power [out]

Pointer to a variable that receives one of the following values.
            

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The device is on.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The device is off.</td>
</tr>
</table>

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -remarks

Not all device types implement this method.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsviddevice-put_power">IMSVidDevice::put_Power</a>