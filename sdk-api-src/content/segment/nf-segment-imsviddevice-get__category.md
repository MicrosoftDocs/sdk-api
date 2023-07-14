---
UID: NF:segment.IMSVidDevice.get__Category
title: IMSVidDevice::get__Category (segment.h)
description: The get__Category method retrieves the category of the device as a GUID.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get__Category method","IMSVidDevice.get__Category","IMSVidDevice::get__Category","IMSVidDeviceget__Category","get__Category","get__Category method [Microsoft TV Technologies]","get__Category method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get__category","segment/IMSVidDevice::get__Category"]
old-location: mstv\imsviddevice_get__category.htm
tech.root: mstv
ms.assetid: 2c5023ee-f38b-48c7-907d-363ca70bf94f
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get__Category method, IMSVidDevice.get__Category, IMSVidDevice::get__Category, IMSVidDeviceget__Category, get__Category, get__Category method [Microsoft TV Technologies], get__Category method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get__category, segment/IMSVidDevice::get__Category
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
 - IMSVidDevice::get__Category
 - segment/IMSVidDevice::get__Category
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
 - IMSVidDevice.get__Category
---

# IMSVidDevice::get__Category


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__Category</b> method retrieves the category of the device as a <b>GUID</b>.

## -parameters

### -param Guid [out]

Pointer to a variable of type <b>GUID</b> that receives the device category.

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

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>