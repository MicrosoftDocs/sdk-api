---
UID: NF:mftransform.IMFDeviceTransform.SetOutputStreamState
title: IMFDeviceTransform::SetOutputStreamState (mftransform.h)
description: The SetOutputStreamState method sets the Device MFT output stream state and media type.
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","SetOutputStreamState method","IMFDeviceTransform.SetOutputStreamState","IMFDeviceTransform::SetOutputStreamState","SetOutputStreamState","SetOutputStreamState method [Streaming Media Devices]","SetOutputStreamState method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::SetOutputStreamState","stream.imfdevicetransform_setoutputstreamstate"]
old-location: stream\imfdevicetransform_setoutputstreamstate.htm
tech.root: stream
ms.assetid: E44A5D0C-440A-4929-9640-AD2F7AA7D19F
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],SetOutputStreamState method, IMFDeviceTransform.SetOutputStreamState, IMFDeviceTransform::SetOutputStreamState, SetOutputStreamState, SetOutputStreamState method [Streaming Media Devices], SetOutputStreamState method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::SetOutputStreamState, stream.imfdevicetransform_setoutputstreamstate
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
 - IMFDeviceTransform::SetOutputStreamState
 - mftransform/IMFDeviceTransform::SetOutputStreamState
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
 - IMFDeviceTransform.SetOutputStreamState
---

# IMFDeviceTransform::SetOutputStreamState


## -description

The <b>SetOutputStreamState</b> method sets the Device MFT output stream state and media type.

## -parameters

### -param dwStreamID [in]

Stream ID of the input stream where the state and media type needs to be changed.

### -param pMediaType [in]

Preferred media type for the input stream is passed in through this parameter. Device MFT should change the media type only if the incoming media type is different from the current media type.

### -param value [in]

Specifies the  <b>DeviceStreamState</b> which the input stream should transition to.

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

This interface method helps to transition the output stream to a specified state with specified media type set on the output stream. This will be used by the DTM when the Device Source requests a specific output stream’s state and media type to be changed. Device MFT should change the specified output stream’s media type and state to the requested media type.

If the incoming media type and stream state are same as the current media type and stream state the method return <b>S_OK</b>.

If the incoming media type and current media type of the stream are the same, Device MFT must change the stream’s state to the requested value and return the appropriate <b>HRESULT</b>.

When a change in the output stream’s media type requires a corresponding change in the input then Device MFT must post the <a href="/windows-hardware/drivers/stream/metransforminputstreamstatechanged">METransformInputStreamStateChanged</a> event  to DTM to change the relevant input stream. The call must return only after changing the input stream’s media type and the appropriate <b>HRESULT</b>.

As an  example, consider a Device MFT that has two input streams and three output streams. Let  Output 1 and Output 2 source from Input 1 and  stream at 720p. Now, let us say Output 2’s media type changes to 1080p. To satisfy this request, Device MFT must  change the Input 1 media type to 1080p, by posting <a href="/windows-hardware/drivers/stream/metransforminputstreamstatechanged">METransformInputStreamStateChanged</a> event to the DTM. DTM would call <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-setinputstreamstate">SetInputStreamState</a> to change the input stream’ media type and state. After this call, the <b>SetOutputStreamState</b> must return.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>