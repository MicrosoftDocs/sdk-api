---
UID: NF:mftransform.IMFDeviceTransform.GetOutputStreamState
title: IMFDeviceTransform::GetOutputStreamState (mftransform.h)
description: The GetOutputStreamState method gets the Device MFT’s output stream state.
helpviewer_keywords: ["GetOutputStreamState","GetOutputStreamState method [Streaming Media Devices]","GetOutputStreamState method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetOutputStreamState method","IMFDeviceTransform.GetOutputStreamState","IMFDeviceTransform::GetOutputStreamState","mftransform/IMFDeviceTransform::GetOutputStreamState","stream.imfdevicetransform_getoutputstreamstate"]
old-location: stream\imfdevicetransform_getoutputstreamstate.htm
tech.root: stream
ms.assetid: A79FC296-7D18-4C74-97E0-F37475AB90D5
ms.date: 12/05/2018
ms.keywords: GetOutputStreamState, GetOutputStreamState method [Streaming Media Devices], GetOutputStreamState method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetOutputStreamState method, IMFDeviceTransform.GetOutputStreamState, IMFDeviceTransform::GetOutputStreamState, mftransform/IMFDeviceTransform::GetOutputStreamState, stream.imfdevicetransform_getoutputstreamstate
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
 - IMFDeviceTransform::GetOutputStreamState
 - mftransform/IMFDeviceTransform::GetOutputStreamState
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
 - IMFDeviceTransform.GetOutputStreamState
---

# IMFDeviceTransform::GetOutputStreamState


## -description

The  <b>GetOutputStreamState</b> method gets the Device MFT’s output stream state.

## -parameters

### -param dwStreamID [in]

Stream ID of the output stream whose state needs to be retrieved.

### -param value [out]

Specifies the current <b>DeviceStreamState</b> of the specified output Device MFT stream.

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
</table>

## -remarks

This method is used by device transform manager (DTM) to get a specific output stream’s state.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>