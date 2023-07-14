---
UID: NF:segment.IMSVidInputDevices.get_Count
title: IMSVidInputDevices::get_Count (segment.h)
description: The get_Count method retrieves the number of items in the collection.
helpviewer_keywords: ["IMSVidInputDevices interface [Microsoft TV Technologies]","get_Count method","IMSVidInputDevices.get_Count","IMSVidInputDevices::get_Count","IMSVidInputDevicesget_Count","get_Count","get_Count method [Microsoft TV Technologies]","get_Count method [Microsoft TV Technologies]","IMSVidInputDevices interface","mstv.imsvidinputdevices_get_count","segment/IMSVidInputDevices::get_Count"]
old-location: mstv\imsvidinputdevices_get_count.htm
tech.root: mstv
ms.assetid: 52c2d9a1-f688-4f5e-a120-082d70f8dff1
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevices interface [Microsoft TV Technologies],get_Count method, IMSVidInputDevices.get_Count, IMSVidInputDevices::get_Count, IMSVidInputDevicesget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IMSVidInputDevices interface, mstv.imsvidinputdevices_get_count, segment/IMSVidInputDevices::get_Count
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
 - IMSVidInputDevices::get_Count
 - segment/IMSVidInputDevices::get_Count
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
 - IMSVidInputDevices.get_Count
---

# IMSVidInputDevices::get_Count


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Count</b> method retrieves the number of items in the collection.

## -parameters

### -param lCount [out]

Pointer to a variable that receives the number of items.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices Interface</a>