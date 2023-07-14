---
UID: NF:segment.IMSVidDevice.get_Status
title: IMSVidDevice::get_Status (segment.h)
description: The get_Status method retrieves status information about the device.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get_Status method","IMSVidDevice.get_Status","IMSVidDevice::get_Status","IMSVidDeviceget_Status","get_Status","get_Status method [Microsoft TV Technologies]","get_Status method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get_status","segment/IMSVidDevice::get_Status"]
old-location: mstv\imsviddevice_get_status.htm
tech.root: mstv
ms.assetid: b11df7f3-d227-4c74-89a3-90716b3b3a12
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Status method, IMSVidDevice.get_Status, IMSVidDevice::get_Status, IMSVidDeviceget_Status, get_Status, get_Status method [Microsoft TV Technologies], get_Status method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_status, segment/IMSVidDevice::get_Status
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
 - IMSVidDevice::get_Status
 - segment/IMSVidDevice::get_Status
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
 - IMSVidDevice.get_Status
---

# IMSVidDevice::get_Status


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Status</b> method retrieves status information about the device.

## -parameters

### -param Status [out]

Pointer to a variable of that receives the current status.

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