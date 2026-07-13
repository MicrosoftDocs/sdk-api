---
UID: NF:segment.IMSVidDevice2.get_DevicePath
title: IMSVidDevice2::get_DevicePath (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
helpviewer_keywords: ["IMSVidDevice2 interface [Microsoft TV Technologies]","get_DevicePath method","IMSVidDevice2.get_DevicePath","IMSVidDevice2::get_DevicePath","IMSVidDevice2get_DevicePath","get_DevicePath","get_DevicePath method [Microsoft TV Technologies]","get_DevicePath method [Microsoft TV Technologies]","IMSVidDevice2 interface","mstv.imsviddevice2_get_devicepath","segment/IMSVidDevice2::get_DevicePath"]
old-location: mstv\imsviddevice2_get_devicepath.htm
tech.root: mstv
ms.assetid: 4a0191d7-2b10-4f7e-96e1-263ddd718229
ms.date: 12/05/2018
ms.keywords: IMSVidDevice2 interface [Microsoft TV Technologies],get_DevicePath method, IMSVidDevice2.get_DevicePath, IMSVidDevice2::get_DevicePath, IMSVidDevice2get_DevicePath, get_DevicePath, get_DevicePath method [Microsoft TV Technologies], get_DevicePath method [Microsoft TV Technologies],IMSVidDevice2 interface, mstv.imsviddevice2_get_devicepath, segment/IMSVidDevice2::get_DevicePath
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidDevice2::get_DevicePath
 - segment/IMSVidDevice2::get_DevicePath
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
 - IMSVidDevice2.get_DevicePath
---

# IMSVidDevice2::get_DevicePath


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        



The <b>get_DevicePath</b> method retrieves the device path.

## -parameters

### -param DevPath [out]

Pointer to a <b>BSTR</b> that receives the device path. The caller must free the returned string, using the <b>SysFreeString</b> function.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

This property is not a human-readable string, but is guaranteed to be unique per device. You can use this property to distinguish between two or more instances of the same model of device.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice2">IMSVidDevice2 Interface</a>