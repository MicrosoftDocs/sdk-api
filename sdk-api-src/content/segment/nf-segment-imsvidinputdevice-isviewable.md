---
UID: NF:segment.IMSVidInputDevice.IsViewable
title: IMSVidInputDevice::IsViewable (segment.h)
description: The IsViewable method determines whether this device can view the specified tune request.
helpviewer_keywords: ["IMSVidInputDevice interface [Microsoft TV Technologies]","IsViewable method","IMSVidInputDevice.IsViewable","IMSVidInputDevice::IsViewable","IMSVidInputDeviceIsViewable","IsViewable","IsViewable method [Microsoft TV Technologies]","IsViewable method [Microsoft TV Technologies]","IMSVidInputDevice interface","mstv.imsvidinputdevice_isviewable","segment/IMSVidInputDevice::IsViewable"]
old-location: mstv\imsvidinputdevice_isviewable.htm
tech.root: mstv
ms.assetid: 4f62bcc4-8c58-4663-9b1f-a5ed7d000a79
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevice interface [Microsoft TV Technologies],IsViewable method, IMSVidInputDevice.IsViewable, IMSVidInputDevice::IsViewable, IMSVidInputDeviceIsViewable, IsViewable, IsViewable method [Microsoft TV Technologies], IsViewable method [Microsoft TV Technologies],IMSVidInputDevice interface, mstv.imsvidinputdevice_isviewable, segment/IMSVidInputDevice::IsViewable
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
 - IMSVidInputDevice::IsViewable
 - segment/IMSVidInputDevice::IsViewable
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
 - IMSVidInputDevice.IsViewable
---

# IMSVidInputDevice::IsViewable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IsViewable</b> method determines whether this device can view the specified tune request.

Currently this method is not implemented by any of the supported input devices.

## -parameters

### -param v [in]

Specifies the tune request as a <b>VARIANT</b> type.

### -param pfViewable [out]

Pointer to variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The device can view this tune request.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The device cannot view this tune request.</td>
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

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice Interface</a>