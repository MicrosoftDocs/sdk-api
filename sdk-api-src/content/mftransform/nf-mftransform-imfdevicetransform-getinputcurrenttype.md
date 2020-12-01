---
UID: NF:mftransform.IMFDeviceTransform.GetInputCurrentType
title: IMFDeviceTransform::GetInputCurrentType (mftransform.h)
description: The GetInputCurrentType method gets the current media type for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetInputCurrentType","GetInputCurrentType method [Streaming Media Devices]","GetInputCurrentType method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetInputCurrentType method","IMFDeviceTransform.GetInputCurrentType","IMFDeviceTransform::GetInputCurrentType","mftransform/IMFDeviceTransform::GetInputCurrentType","stream.imfdevicetransform_getinputcurrenttype"]
old-location: stream\imfdevicetransform_getinputcurrenttype.htm
tech.root: stream
ms.assetid: 8E2955AD-ECBD-4C24-972A-8F670DC08F0F
ms.date: 12/05/2018
ms.keywords: GetInputCurrentType, GetInputCurrentType method [Streaming Media Devices], GetInputCurrentType method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetInputCurrentType method, IMFDeviceTransform.GetInputCurrentType, IMFDeviceTransform::GetInputCurrentType, mftransform/IMFDeviceTransform::GetInputCurrentType, stream.imfdevicetransform_getinputcurrenttype
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
 - IMFDeviceTransform::GetInputCurrentType
 - mftransform/IMFDeviceTransform::GetInputCurrentType
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
 - IMFDeviceTransform.GetInputCurrentType
---

# IMFDeviceTransform::GetInputCurrentType


## -description

The <b>GetInputCurrentType</b> method gets the current media type for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamids">IMFDeviceTransform::GetStreamIDs</a>.

### -param pMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface that represents the current type used by that stream.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
No media type has been set yet.

</td>
</tr>
</table>

## -remarks

If the specified input stream does not yet have a media type, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>. 

<h3><a id="Implementation_notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation notes</h3>
The MFT should return a clone of the media type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>