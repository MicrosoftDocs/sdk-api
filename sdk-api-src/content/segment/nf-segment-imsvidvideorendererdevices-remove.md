---
UID: NF:segment.IMSVidVideoRendererDevices.Remove
title: IMSVidVideoRendererDevices::Remove (segment.h)
description: The Remove method removes an item from the collection.
helpviewer_keywords: ["IMSVidVideoRendererDevices interface [Microsoft TV Technologies]","Remove method","IMSVidVideoRendererDevices.Remove","IMSVidVideoRendererDevices::Remove","IMSVidVideoRendererDevicesRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","IMSVidVideoRendererDevices interface","mstv.imsvidvideorendererdevices_remove","segment/IMSVidVideoRendererDevices::Remove"]
old-location: mstv\imsvidvideorendererdevices_remove.htm
tech.root: mstv
ms.assetid: 0a1d8f8b-1e62-470d-8f94-afc238755cad
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRendererDevices interface [Microsoft TV Technologies],Remove method, IMSVidVideoRendererDevices.Remove, IMSVidVideoRendererDevices::Remove, IMSVidVideoRendererDevicesRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IMSVidVideoRendererDevices interface, mstv.imsvidvideorendererdevices_remove, segment/IMSVidVideoRendererDevices::Remove
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
 - IMSVidVideoRendererDevices::Remove
 - segment/IMSVidVideoRendererDevices::Remove
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
 - IMSVidVideoRendererDevices.Remove
---

# IMSVidVideoRendererDevices::Remove


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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
The index is out of range.

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
The collection is read-only; cannot remove any items.

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

The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorendererdevices-get_count">IMSVidVideoRendererDevices::get_Count</a> - 1.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorendererdevices">IMSVidVideoRendererDevices Interface</a>