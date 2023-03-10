---
UID: NF:mftransform.IMFDeviceTransform.GetOutputAvailableType
title: IMFDeviceTransform::GetOutputAvailableType (mftransform.h)
description: The GetOutputAvailableType method gets an available media type for an output stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetOutputAvailableType","GetOutputAvailableType method [Streaming Media Devices]","GetOutputAvailableType method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetOutputAvailableType method","IMFDeviceTransform.GetOutputAvailableType","IMFDeviceTransform::GetOutputAvailableType","mftransform/IMFDeviceTransform::GetOutputAvailableType","stream.imfdevicetransform_getoutputavailabletype"]
old-location: stream\imfdevicetransform_getoutputavailabletype.htm
tech.root: stream
ms.assetid: B4224C70-5864-4AE3-8388-2B9A62517B62
ms.date: 12/05/2018
ms.keywords: GetOutputAvailableType, GetOutputAvailableType method [Streaming Media Devices], GetOutputAvailableType method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetOutputAvailableType method, IMFDeviceTransform.GetOutputAvailableType, IMFDeviceTransform::GetOutputAvailableType, mftransform/IMFDeviceTransform::GetOutputAvailableType, stream.imfdevicetransform_getoutputavailabletype
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFDeviceTransform::GetOutputAvailableType
 - mftransform/IMFDeviceTransform::GetOutputAvailableType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.GetOutputAvailableType
---

# IMFDeviceTransform::GetOutputAvailableType


## -description

The <b>GetOutputAvailableType</b> method gets an available media type for an output stream on this Media Foundation transform (MFT).

## -parameters

### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamids">IMFDeviceTransform::GetStreamIDs</a>.

### -param dwTypeIndex [in]

Index of the media type to retrieve. Media types are indexed from zero and returned in approximate order of preference.

### -param pMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include but not limited to values given in the following table.

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
Initialization succeeded

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Device MFT could not  support the request at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
There is no media type available with the specified index.

</td>
</tr>
</table>

## -remarks

The MFT defines a list of available media types for each output stream and orders them by preference.

This method enumerates the available media types for an output stream. To enumerate the available types, increment <i>dwTypeIndex</i> until the method returns <b>MF_E_NO_MORE_TYPES</b>.

<h3><a id="Implementation_notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation notes</h3>
If the MFT stores a media type internally, the MFT should return a clone of the media type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>