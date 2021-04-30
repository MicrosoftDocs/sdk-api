---
UID: NF:segment.IMSVidInputDevices.Remove
title: IMSVidInputDevices::Remove (segment.h)
description: The Remove method removes an item from the collection.
helpviewer_keywords: ["IMSVidInputDevices interface [Microsoft TV Technologies]","Remove method","IMSVidInputDevices.Remove","IMSVidInputDevices::Remove","IMSVidInputDevicesRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","IMSVidInputDevices interface","mstv.imsvidinputdevices_remove","segment/IMSVidInputDevices::Remove"]
old-location: mstv\imsvidinputdevices_remove.htm
tech.root: mstv
ms.assetid: c8990564-70d3-4962-9ff2-24664dbc1161
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevices interface [Microsoft TV Technologies],Remove method, IMSVidInputDevices.Remove, IMSVidInputDevices::Remove, IMSVidInputDevicesRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IMSVidInputDevices interface, mstv.imsvidinputdevices_remove, segment/IMSVidInputDevices::Remove
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
 - IMSVidInputDevices::Remove
 - segment/IMSVidInputDevices::Remove
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
 - IMSVidInputDevices.Remove
---

# IMSVidInputDevices::Remove


## -description

The <b>Remove</b> method removes an item from the collection.

## -parameters

### -param v [in]

<b>VARIANT</b> that specifies the index of the item to remove.

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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Wrong <b>VARIANT</b> type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This collection is read-only; no items can be removed from it

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>

## -remarks

The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-get_count">IMSVidInputDevices::get_Count</a> - 1.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-add">IMSVidInputDevices::Add</a>