---
UID: NF:segment.IMSVidDevice.put_Power
title: IMSVidDevice::put_Power (segment.h)
description: The put_Power method turns the device on or off.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","put_Power method","IMSVidDevice.put_Power","IMSVidDevice::put_Power","IMSVidDeviceput_Power","mstv.imsviddevice_put_power","put_Power","put_Power method [Microsoft TV Technologies]","put_Power method [Microsoft TV Technologies]","IMSVidDevice interface","segment/IMSVidDevice::put_Power"]
old-location: mstv\imsviddevice_put_power.htm
tech.root: mstv
ms.assetid: 6a0122a8-6015-4255-a7d6-ab72b4025bd6
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],put_Power method, IMSVidDevice.put_Power, IMSVidDevice::put_Power, IMSVidDeviceput_Power, mstv.imsviddevice_put_power, put_Power, put_Power method [Microsoft TV Technologies], put_Power method [Microsoft TV Technologies],IMSVidDevice interface, segment/IMSVidDevice::put_Power
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
 - IMSVidDevice::put_Power
 - segment/IMSVidDevice::put_Power
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
 - IMSVidDevice.put_Power
---

# IMSVidDevice::put_Power


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Power</b> method turns the device on or off.

## -parameters

### -param Power [in]

Specifies whether to turn the power on or off. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Turn the device on.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Turn the device off.</td>
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
</table>

## -remarks

Not all device types implement this method.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get_power">IMSVidDevice::get_Power</a>