---
UID: NF:mftransform.IMFDeviceTransform.GetInputStreamPreferredState
title: IMFDeviceTransform::GetInputStreamPreferredState (mftransform.h)
description: The GetInputStreamPreferredState method gets a Device MFT input stream’s preferred state and media type.
helpviewer_keywords: ["GetInputStreamPreferredState","GetInputStreamPreferredState method [Streaming Media Devices]","GetInputStreamPreferredState method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetInputStreamPreferredState method","IMFDeviceTransform.GetInputStreamPreferredState","IMFDeviceTransform::GetInputStreamPreferredState","mftransform/IMFDeviceTransform::GetInputStreamPreferredState","stream.imfdevicetransform_getinputstreampreferredstate"]
old-location: stream\imfdevicetransform_getinputstreampreferredstate.htm
tech.root: stream
ms.assetid: 56334B73-DCBC-4999-9685-2489D6C15E2E
ms.date: 12/05/2018
ms.keywords: GetInputStreamPreferredState, GetInputStreamPreferredState method [Streaming Media Devices], GetInputStreamPreferredState method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetInputStreamPreferredState method, IMFDeviceTransform.GetInputStreamPreferredState, IMFDeviceTransform::GetInputStreamPreferredState, mftransform/IMFDeviceTransform::GetInputStreamPreferredState, stream.imfdevicetransform_getinputstreampreferredstate
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
 - IMFDeviceTransform::GetInputStreamPreferredState
 - mftransform/IMFDeviceTransform::GetInputStreamPreferredState
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
 - IMFDeviceTransform.GetInputStreamPreferredState
---

# IMFDeviceTransform::GetInputStreamPreferredState


## -description

The <b>GetInputStreamPreferredState</b> method gets a Device MFT input stream’s preferred state and media type.

## -parameters

### -param dwStreamID [in]

Stream ID of the input stream whose state needs to be retrieved.

### -param value [out]

Specifies the current <b>DeviceStreamState</b> of the specified input Device MFT stream.

### -param ppMediaType [out]

Preferred media type for the input stream is passed in through this parameter.

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
</table>

## -remarks

This interface function helps to query the Device MFT input stream’s preferred state and mediatype to which it needs to be transitioned.

When a change in the output stream’s media type needs corresponding change in the input, then Device MFT would post <a href="/windows-hardware/drivers/stream/metransforminputstreamstatechanged">METransformInputStreamStateChanged</a> to DTM to change the relevant input stream. DTM would call <b>GetInputStreamPreferredState</b> to retrieve Device MFT input stream’s preferred mediatype and state.

As an  example, consider a Device MFT that has two input streams and three output streams. Let  Output 1 and Output 2 source from Input 1 and  stream at 720p. Now, let us say Output 2’s media type changes to 1080p. To satisfy this request, Device MFT must  change the Input 1 media type to 1080p, by posting <a href="/windows-hardware/drivers/stream/metransforminputstreamstatechanged">METransformInputStreamStateChanged</a> event to the DTM. DTM would call <b>GetInputStreamPreferredState</b> and retrieve the preferred state and mediatype. DTM would call  <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-setinputstreamstate">SetInputStreamState</a> to change the input stream’ mediatype and state.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>