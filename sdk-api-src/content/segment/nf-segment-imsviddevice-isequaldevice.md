---
UID: NF:segment.IMSVidDevice.IsEqualDevice
title: IMSVidDevice::IsEqualDevice (segment.h)
description: The IsEqualDevice method queries whether this device and another device represent the same underlying hardware.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","IsEqualDevice method","IMSVidDevice.IsEqualDevice","IMSVidDevice::IsEqualDevice","IMSVidDeviceIsEqualDevice","IsEqualDevice","IsEqualDevice method [Microsoft TV Technologies]","IsEqualDevice method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_isequaldevice","segment/IMSVidDevice::IsEqualDevice"]
old-location: mstv\imsviddevice_isequaldevice.htm
tech.root: mstv
ms.assetid: b0f59466-7a2a-453e-999c-c7ebf126d18b
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],IsEqualDevice method, IMSVidDevice.IsEqualDevice, IMSVidDevice::IsEqualDevice, IMSVidDeviceIsEqualDevice, IsEqualDevice, IsEqualDevice method [Microsoft TV Technologies], IsEqualDevice method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_isequaldevice, segment/IMSVidDevice::IsEqualDevice
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
 - IMSVidDevice::IsEqualDevice
 - segment/IMSVidDevice::IsEqualDevice
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
 - IMSVidDevice.IsEqualDevice
---

# IMSVidDevice::IsEqualDevice


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IsEqualDevice</b> method queries whether this device and another device represent the same underlying hardware.

## -parameters

### -param Device [in]

Pointer to the other device's <a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice</a> interface.

### -param IsEqual [out]

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
<td>The two devices represent the same underlying hardware.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The two devices do not represent the same hardware.</td>
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
Success; returned VARIANT_TRUE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Success; returned VARIANT_FALSE.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>