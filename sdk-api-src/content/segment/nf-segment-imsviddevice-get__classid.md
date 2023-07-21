---
UID: NF:segment.IMSVidDevice.get__ClassID
title: IMSVidDevice::get__ClassID (segment.h)
description: The get__ClassID method retrieves the device's class identifier (CLSID) as a GUID.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get__ClassID method","IMSVidDevice.get__ClassID","IMSVidDevice::get__ClassID","IMSVidDeviceget__ClassID","get__ClassID","get__ClassID method [Microsoft TV Technologies]","get__ClassID method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get__classid","segment/IMSVidDevice::get__ClassID"]
old-location: mstv\imsviddevice_get__classid.htm
tech.root: mstv
ms.assetid: 80890372-2d92-4a3a-963f-2a6ca6632c52
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get__ClassID method, IMSVidDevice.get__ClassID, IMSVidDevice::get__ClassID, IMSVidDeviceget__ClassID, get__ClassID, get__ClassID method [Microsoft TV Technologies], get__ClassID method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get__classid, segment/IMSVidDevice::get__ClassID
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
 - IMSVidDevice::get__ClassID
 - segment/IMSVidDevice::get__ClassID
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
 - IMSVidDevice.get__ClassID
---

# IMSVidDevice::get__ClassID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__ClassID</b> method retrieves the device's class identifier (CLSID) as a <b>GUID</b>.

## -parameters

### -param Clsid [out]

Pointer to a variable of type <b>GUID</b> that receives the CLSID.

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