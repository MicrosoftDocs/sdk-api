---
UID: NF:mftransform.IMFDeviceTransform.ProcessEvent
title: IMFDeviceTransform::ProcessEvent (mftransform.h)
description: The ProcessEvent method sends an event to an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","ProcessEvent method","IMFDeviceTransform.ProcessEvent","IMFDeviceTransform::ProcessEvent","ProcessEvent","ProcessEvent method [Streaming Media Devices]","ProcessEvent method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::ProcessEvent","stream.imfdevicetransform_processevent"]
old-location: stream\imfdevicetransform_processevent.htm
tech.root: stream
ms.assetid: 6E8B208C-A492-41C8-9A86-34B11375053B
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],ProcessEvent method, IMFDeviceTransform.ProcessEvent, IMFDeviceTransform::ProcessEvent, ProcessEvent, ProcessEvent method [Streaming Media Devices], ProcessEvent method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::ProcessEvent, stream.imfdevicetransform_processevent
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
 - IMFDeviceTransform::ProcessEvent
 - mftransform/IMFDeviceTransform::ProcessEvent
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
 - IMFDeviceTransform.ProcessEvent
---

# IMFDeviceTransform::ProcessEvent


## -description

The <b>ProcessEvent</b> method sends an event to an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamids">IMFDeviceTransform::GetStreamIDs</a>.

### -param pEvent [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of an event object.

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
The event processed successfully. The event will be propagated down stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
An invalid stream ID was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_TRANSFORM_DO_NO_PROPOGATE_EVENT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the Device MFT does not want the event to be propagated further.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The function is not implemented.

</td>
</tr>
</table>

## -remarks

An MFT can handle sending the event downstream, or it can let the DTM do this, as indicated by the return value:

<ul>
<li><b>E_NOTIMPL:</b> The MFT ignores all events, and the DTM should send all events downstream. After the pipeline receives this return value</li>
<li><b>S_OK: </b>The MFT has examined this event, but the DTM should send the event downstream. Internally, the MFT might respond to the event in some way, or it might ignore the event. </li>
<li><b>MF_S_TRANSFORM_DO_NOT_PROPAGATE_EVENT:</b> The DTM should not propagate this event downstream. Either the MFT will send the event downstream, or else the MFT will consume the event and not send it downstream. The MFT should only consume the event if the event should stop at this MFT and not travel any further downstream. But in most cases, the event should travel downstream. </li>
</ul>
To send the event downstream, the MFT adds the event to the collection object that is provided by the client in the pEvents member of the <b>MFT_OUTPUT_DATA_BUFFER</b> structure, when the client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processoutput">IMFTransform::ProcessOutput</a>. 

Events must be serialized with the samples that come before and after them. Attach the event to the output sample that follows the event. (The pipeline will process the event first, and then the sample.) If an MFT holds back one or more samples between calls to <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processinput">IMFTransform::ProcessInput</a> and <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-processoutput">IMFTransform::ProcessOutput</a>, the MFT should handle sending all events downstream, because in this situation the pipeline cannot correlate input samples with output samples.

If an MFT does not hold back samples and does not need to examine any events, it can return <b>E_NOTIMPL</b>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>