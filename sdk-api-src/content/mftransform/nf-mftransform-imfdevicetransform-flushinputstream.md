---
UID: NF:mftransform.IMFDeviceTransform.FlushInputStream
title: IMFDeviceTransform::FlushInputStream (mftransform.h)
description: The FlushInputStream method flushes a Device MFT’s input stream.
helpviewer_keywords: ["FlushInputStream","FlushInputStream method [Streaming Media Devices]","FlushInputStream method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","FlushInputStream method","IMFDeviceTransform.FlushInputStream","IMFDeviceTransform::FlushInputStream","mftransform/IMFDeviceTransform::FlushInputStream","stream.imfdevicetransform_flushinputstream"]
old-location: stream\imfdevicetransform_flushinputstream.htm
tech.root: stream
ms.assetid: 646A9446-B87A-40B5-8A0F-9DE67286825B
ms.date: 12/05/2018
ms.keywords: FlushInputStream, FlushInputStream method [Streaming Media Devices], FlushInputStream method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],FlushInputStream method, IMFDeviceTransform.FlushInputStream, IMFDeviceTransform::FlushInputStream, mftransform/IMFDeviceTransform::FlushInputStream, stream.imfdevicetransform_flushinputstream
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
 - IMFDeviceTransform::FlushInputStream
 - mftransform/IMFDeviceTransform::FlushInputStream
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
 - IMFDeviceTransform.FlushInputStream
---

# IMFDeviceTransform::FlushInputStream


## -description

The <b>FlushInputStream</b> method flushes a Device MFT’s input stream.

## -parameters

### -param dwStreamIndex [in]

Stream ID of the input stream which needs to be flushed.

### -param dwFlags [in]

Contains the <b>HRESULT</b> of flushing the corresponding devproxy output stream.

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

This interface method helps to flush a Device MFT’s input stream.

Device MFT should drop all samples in its queues and reset all its internal data structures related to that input stream. This is equivalent to resetting the input stream. The media type and stream state must not change.

<h3><a id="When_called"></a><a id="when_called"></a><a id="WHEN_CALLED"></a>When called</h3>
When the input stream needs to be reset, device transform manager (DTM) would call this method.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>