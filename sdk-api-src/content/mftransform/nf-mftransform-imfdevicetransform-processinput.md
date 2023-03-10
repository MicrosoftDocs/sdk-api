---
UID: NF:mftransform.IMFDeviceTransform.ProcessInput
title: IMFDeviceTransform::ProcessInput (mftransform.h)
description: The ProcessInput method delivers data to an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","ProcessInput method","IMFDeviceTransform.ProcessInput","IMFDeviceTransform::ProcessInput","ProcessInput","ProcessInput method [Streaming Media Devices]","ProcessInput method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::ProcessInput","stream.imfdevicetransform_processinput"]
old-location: stream\imfdevicetransform_processinput.htm
tech.root: stream
ms.assetid: EB4197BA-5963-45E7-B196-94F907637EBB
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],ProcessInput method, IMFDeviceTransform.ProcessInput, IMFDeviceTransform::ProcessInput, ProcessInput, ProcessInput method [Streaming Media Devices], ProcessInput method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::ProcessInput, stream.imfdevicetransform_processinput
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
 - IMFDeviceTransform::ProcessInput
 - mftransform/IMFDeviceTransform::ProcessInput
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
 - IMFDeviceTransform.ProcessInput
---

# IMFDeviceTransform::ProcessInput


## -description

The <b>ProcessInput</b> method delivers data to an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier.

### -param pSample [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the input sample. The sample must contain at least one media buffer that contains valid input data.

### -param dwFlags [in]

Must be zero.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument passed.

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
<dt><b>MF_E_INVAILIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
An invalid stream ID was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALID_STREAM_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested stream transition is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
Input media type has not been set.

</td>
</tr>
</table>

## -remarks

In most cases, if the method succeeds, the MFT stores the sample and holds a reference count on the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> pointer. When the MFT is done using the sample it must release it to avoid a memory leak.

After the DTM has set valid media types on all of the streams, the MFT should always be able to accept more input and be able to produce more output. 

If an MFT encounters a non-fatal error in the input data, it can simply drop the data and attempt to recover when it gets the more input data. If the MFT drops any data, it should set the <a href="/windows/desktop/medfound/mfsampleextension-discontinuity-attribute">MFSampleExtension_Discontinuity</a> attribute on the next output sample, to notify the caller that there is a gap in the data stream.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>