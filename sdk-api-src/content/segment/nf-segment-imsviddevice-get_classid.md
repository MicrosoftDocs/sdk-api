---
UID: NF:segment.IMSVidDevice.get_ClassID
title: IMSVidDevice::get_ClassID (segment.h)
description: The get_ClassID method retrieves the device's class identifier (CLSID) as a BSTR.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get_ClassID method","IMSVidDevice.get_ClassID","IMSVidDevice::get_ClassID","IMSVidDeviceget_ClassID","get_ClassID","get_ClassID method [Microsoft TV Technologies]","get_ClassID method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get_classid","segment/IMSVidDevice::get_ClassID"]
old-location: mstv\imsviddevice_get_classid.htm
tech.root: mstv
ms.assetid: 78910e3d-bd00-48c5-b1be-504dc92280a0
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_ClassID method, IMSVidDevice.get_ClassID, IMSVidDevice::get_ClassID, IMSVidDeviceget_ClassID, get_ClassID, get_ClassID method [Microsoft TV Technologies], get_ClassID method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_classid, segment/IMSVidDevice::get_ClassID
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
 - IMSVidDevice::get_ClassID
 - segment/IMSVidDevice::get_ClassID
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
 - IMSVidDevice.get_ClassID
---

# IMSVidDevice::get_ClassID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ClassID</b> method retrieves the device's class identifier (CLSID) as a <b>BSTR</b>.

## -parameters

### -param Clsid [out]

Pointer to a variable that receives a string representation of the CLSID.

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

This method is provided for Automation clients. C++ applications can use the <a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get__classid">IMSVidDevice::get__ClassID</a> method, which returns a <b>GUID</b> rather than a <b>BSTR</b>.

The caller must free the returned string, using the <b>SysFreeString</b> function.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>