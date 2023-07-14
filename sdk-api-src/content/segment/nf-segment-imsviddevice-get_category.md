---
UID: NF:segment.IMSVidDevice.get_Category
title: IMSVidDevice::get_Category (segment.h)
description: The get_Category method retrieves the category of the device as a BSTR.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get_Category method","IMSVidDevice.get_Category","IMSVidDevice::get_Category","IMSVidDeviceget_Category","get_Category","get_Category method [Microsoft TV Technologies]","get_Category method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get_category","segment/IMSVidDevice::get_Category"]
old-location: mstv\imsviddevice_get_category.htm
tech.root: mstv
ms.assetid: 369080c6-b707-494e-a663-e78e7d8d3eaf
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Category method, IMSVidDevice.get_Category, IMSVidDevice::get_Category, IMSVidDeviceget_Category, get_Category, get_Category method [Microsoft TV Technologies], get_Category method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_category, segment/IMSVidDevice::get_Category
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
 - IMSVidDevice::get_Category
 - segment/IMSVidDevice::get_Category
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
 - IMSVidDevice.get_Category
---

# IMSVidDevice::get_Category


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Category</b> method retrieves the category of the device as a <b>BSTR</b>.

## -parameters

### -param Guid [out]

<b>BSTR</b> that receives the device category.

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

## -remarks

The device category is identified by a <b>GUID</b>. This method returns a string representation of the <b>GUID</b>.

This method is provided for Automation clients. C++ applications can use the <a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get__category">IMSVidDevice::get__Category</a> method, which returns a <b>GUID</b> rather than a <b>BSTR</b>.

The caller must free the returned string, using the <b>SysFreeString</b> function.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>