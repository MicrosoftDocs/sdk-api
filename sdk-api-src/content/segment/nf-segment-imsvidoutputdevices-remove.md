---
UID: NF:segment.IMSVidOutputDevices.Remove
title: IMSVidOutputDevices::Remove (segment.h)
description: The Remove method removes an item from the collection.
helpviewer_keywords: ["IMSVidOutputDevices interface [Microsoft TV Technologies]","Remove method","IMSVidOutputDevices.Remove","IMSVidOutputDevices::Remove","IMSVidOutputDevicesRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","IMSVidOutputDevices interface","mstv.imsvidoutputdevices_remove","segment/IMSVidOutputDevices::Remove"]
old-location: mstv\imsvidoutputdevices_remove.htm
tech.root: mstv
ms.assetid: 40c4bc6b-091b-44b5-a313-5db20842adcf
ms.date: 12/05/2018
ms.keywords: IMSVidOutputDevices interface [Microsoft TV Technologies],Remove method, IMSVidOutputDevices.Remove, IMSVidOutputDevices::Remove, IMSVidOutputDevicesRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IMSVidOutputDevices interface, mstv.imsvidoutputdevices_remove, segment/IMSVidOutputDevices::Remove
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
 - IMSVidOutputDevices::Remove
 - segment/IMSVidOutputDevices::Remove
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
 - IMSVidOutputDevices.Remove
---

# IMSVidOutputDevices::Remove


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

The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <code>IMSVidOutputDevices::get_Count - 1</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidoutputdevices">IMSVidOutputDevices Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidoutputdevices-add">IMSVidOutputDevices::Add</a>