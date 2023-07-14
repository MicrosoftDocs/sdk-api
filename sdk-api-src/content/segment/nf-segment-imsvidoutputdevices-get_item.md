---
UID: NF:segment.IMSVidOutputDevices.get_Item
title: IMSVidOutputDevices::get_Item (segment.h)
description: The get_Item method retrieves the specified item from the collection.
helpviewer_keywords: ["IMSVidOutputDevices interface [Microsoft TV Technologies]","get_Item method","IMSVidOutputDevices.get_Item","IMSVidOutputDevices::get_Item","IMSVidOutputDevicesget_Item","get_Item","get_Item method [Microsoft TV Technologies]","get_Item method [Microsoft TV Technologies]","IMSVidOutputDevices interface","mstv.imsvidoutputdevices_get_item","segment/IMSVidOutputDevices::get_Item"]
old-location: mstv\imsvidoutputdevices_get_item.htm
tech.root: mstv
ms.assetid: 373dd785-3671-4afa-92ac-e61a39a68228
ms.date: 12/05/2018
ms.keywords: IMSVidOutputDevices interface [Microsoft TV Technologies],get_Item method, IMSVidOutputDevices.get_Item, IMSVidOutputDevices::get_Item, IMSVidOutputDevicesget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],IMSVidOutputDevices interface, mstv.imsvidoutputdevices_get_item, segment/IMSVidOutputDevices::get_Item
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
 - IMSVidOutputDevices::get_Item
 - segment/IMSVidOutputDevices::get_Item
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
 - IMSVidOutputDevices.get_Item
---

# IMSVidOutputDevices::get_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Item</b> method retrieves the specified item from the collection.

## -parameters

### -param v [in]

<b>VARIANT</b> that specifies the index of the item to retrieve.

### -param pDB [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a> interface pointer.

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
Unexpected error.

</td>
</tr>
</table>

## -remarks

The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <code>IMSVidOutputDevices::get_Count - 1</code>.

If the method succeeds, the <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevice">IMSVidOutputDevice</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidoutputdevices">IMSVidOutputDevices Interface</a>