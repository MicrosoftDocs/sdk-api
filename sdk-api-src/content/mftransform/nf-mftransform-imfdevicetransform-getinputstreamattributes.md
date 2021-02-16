---
UID: NF:mftransform.IMFDeviceTransform.GetInputStreamAttributes
title: IMFDeviceTransform::GetInputStreamAttributes (mftransform.h)
description: The GetInputStreamAttributes method gets the attribute store for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetInputStreamAttributes","GetInputStreamAttributes method [Streaming Media Devices]","GetInputStreamAttributes method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetInputStreamAttributes method","IMFDeviceTransform.GetInputStreamAttributes","IMFDeviceTransform::GetInputStreamAttributes","mftransform/IMFDeviceTransform::GetInputStreamAttributes","stream.imfdevicetransform_getinputstreamattributes"]
old-location: stream\imfdevicetransform_getinputstreamattributes.htm
tech.root: stream
ms.assetid: 087696C2-BD29-4BAE-8285-1B127E0D076E
ms.date: 12/05/2018
ms.keywords: GetInputStreamAttributes, GetInputStreamAttributes method [Streaming Media Devices], GetInputStreamAttributes method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetInputStreamAttributes method, IMFDeviceTransform.GetInputStreamAttributes, IMFDeviceTransform::GetInputStreamAttributes, mftransform/IMFDeviceTransform::GetInputStreamAttributes, stream.imfdevicetransform_getinputstreamattributes
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
 - IMFDeviceTransform::GetInputStreamAttributes
 - mftransform/IMFDeviceTransform::GetInputStreamAttributes
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
 - IMFDeviceTransform.GetInputStreamAttributes
---

# IMFDeviceTransform::GetInputStreamAttributes


## -description

The <b>GetInputStreamAttributes</b> method gets the attribute store for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Stream ID of the input stream whose state needs to be retrieved.

### -param ppAttributes [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. The caller must release the interface.

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
Transitioning the stream state succeeded.

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
</table>

## -remarks

This method  is used by DTM to get a specific input stream’s attribute store.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>