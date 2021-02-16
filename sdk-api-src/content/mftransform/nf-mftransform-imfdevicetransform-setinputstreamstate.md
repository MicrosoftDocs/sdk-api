---
UID: NF:mftransform.IMFDeviceTransform.SetInputStreamState
title: IMFDeviceTransform::SetInputStreamState (mftransform.h)
description: The SetInputStreamState method sets the Device MFT input stream state and media type.
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","SetInputStreamState method","IMFDeviceTransform.SetInputStreamState","IMFDeviceTransform::SetInputStreamState","SetInputStreamState","SetInputStreamState method [Streaming Media Devices]","SetInputStreamState method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::SetInputStreamState","stream.imfdevicetransform_setinputstreamstate"]
old-location: stream\imfdevicetransform_setinputstreamstate.htm
tech.root: stream
ms.assetid: 010E482E-7464-45AE-80B6-9456864E1C96
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],SetInputStreamState method, IMFDeviceTransform.SetInputStreamState, IMFDeviceTransform::SetInputStreamState, SetInputStreamState, SetInputStreamState method [Streaming Media Devices], SetInputStreamState method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::SetInputStreamState, stream.imfdevicetransform_setinputstreamstate
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
 - IMFDeviceTransform::SetInputStreamState
 - mftransform/IMFDeviceTransform::SetInputStreamState
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
 - IMFDeviceTransform.SetInputStreamState
---

# IMFDeviceTransform::SetInputStreamState


## -description

The <b>SetInputStreamState</b> method sets the Device MFT input stream state and media type.

## -parameters

### -param dwStreamID [in]

Stream ID of the input stream where the state and media type needs to be changed.

### -param pMediaType [in]

Preferred media type for the input stream is passed in through this parameter. Device MFT should change the media type only if the incoming media type is different from the current media type.

### -param value [in]

Specifies the  <b>DeviceStreamState</b> which the input stream should transition to.

### -param dwFlags [in]

When  <b>S_OK</b> is returned, perform the state change operation. Otherwise, this contains an error that occurred while setting the media type on the devproxy  output pin. In this case, propagate the error appropriately.

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

This interface function helps to transition the input stream to a specified state with a specified media type set on the input stream. This will be used by device transform  manager (DTM) when the Device MFT requests a specific input stream’s state and media type to be changed. Device MFT would need to request such a change when one of the Device MFT's output changes.

As an  example, consider a Device MFT that has two input streams and three output streams. Let  Output 1 and Output 2 source from Input 1 and  stream at 720p. Now, if   Output 2’s media type changes to 1080p, Device MFT has to change Input 1's media type to 1080p. To achieve this, Device MFT should request DTM to call this method using the <a href="/windows-hardware/drivers/stream/metransforminputstreamstatechanged">METransformInputStreamStateChanged</a> message.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>