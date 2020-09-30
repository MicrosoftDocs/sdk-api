---
UID: NN:segment.IMSVidInputDevices
title: IMSVidInputDevices (segment.h)
description: The IMSVidInputDevices interface represents a collection of input devices. The MSVidInputDevices object exposes this object.
helpviewer_keywords: ["IMSVidInputDevices","IMSVidInputDevices interface [Microsoft TV Technologies]","IMSVidInputDevices interface [Microsoft TV Technologies]","described","IMSVidInputDevicesInterface","mstv.imsvidinputdevices","segment/IMSVidInputDevices"]
old-location: mstv\imsvidinputdevices.htm
tech.root: mstv
ms.assetid: cb9d9885-718e-43b9-b195-66149bd7e973
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevices, IMSVidInputDevices interface [Microsoft TV Technologies], IMSVidInputDevices interface [Microsoft TV Technologies],described, IMSVidInputDevicesInterface, mstv.imsvidinputdevices, segment/IMSVidInputDevices
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
 - IMSVidInputDevices
 - segment/IMSVidInputDevices
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
 - IMSVidInputDevices
---

# IMSVidInputDevices interface


## -description

The <b>IMSVidInputDevices</b> interface represents a collection of input devices. The <a href="/previous-versions/windows/desktop/legacy/dd695130(v=vs.85)">MSVidInputDevices</a> object exposes this object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidInputDevices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidInputDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidInputDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-add">Add</a>
</td>
<td align="left" width="63%">
Adds an input device to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidinputdevices-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidInputDevices)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>