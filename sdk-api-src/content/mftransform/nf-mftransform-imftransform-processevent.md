---
UID: NF:mftransform.IMFTransform.ProcessEvent
title: IMFTransform::ProcessEvent (mftransform.h)
description: Sends an event to an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["28366df3-c414-45ff-bb15-c5483f11de85","IMFTransform interface [Media Foundation]","ProcessEvent method","IMFTransform.ProcessEvent","IMFTransform::ProcessEvent","ProcessEvent","ProcessEvent method [Media Foundation]","ProcessEvent method [Media Foundation]","IMFTransform interface","mf.imftransform_processevent","mftransform/IMFTransform::ProcessEvent"]
old-location: mf\imftransform_processevent.htm
tech.root: mf
ms.assetid: 28366df3-c414-45ff-bb15-c5483f11de85
ms.date: 12/05/2018
ms.keywords: 28366df3-c414-45ff-bb15-c5483f11de85, IMFTransform interface [Media Foundation],ProcessEvent method, IMFTransform.ProcessEvent, IMFTransform::ProcessEvent, ProcessEvent, ProcessEvent method [Media Foundation], ProcessEvent method [Media Foundation],IMFTransform interface, mf.imftransform_processevent, mftransform/IMFTransform::ProcessEvent
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTransform::ProcessEvent
 - mftransform/IMFTransform::ProcessEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.ProcessEvent
---

# IMFTransform::ProcessEvent


## -description

Sends an event to an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param pEvent [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of an event object.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type is not set on one or more streams.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_TRANSFORM_DO_NOT_PROPAGATE_EVENT</b></dt>
</dl>
</td>
<td width="60%">
The pipeline should not propagate the event.
              

</td>
</tr>
</table>

## -remarks

An MFT can handle sending the event downstream, or it can let the pipeline do this, as indicated by the return value:
      

<ul>
<li><b>E_NOTIMPL</b>: The MFT ignores all events, and the pipeline should send all events downstream. After the pipeline receives this return value, it might not call <b>ProcessEvent</b> again.
          </li>
<li><b>S_OK</b>: The MFT has examined this event, but the pipeline should send the event downstream. Internally, the MFT might respond to the event in some way, or it might ignore the event.
          </li>
<li><b>MF_S_TRANSFORM_DO_NOT_PROPAGATE_EVENT</b>: The pipeline should not propagate this event downstream. Either the MFT will send the event downstream, or else the MFT will consume the event and not send it downstream. The MFT should only consume the event if the event should stop at this MFT and not travel any further downstream. But in most cases, the event should travel downstream.
          </li>
</ul>
To send the event downstream, the MFT adds the event to the collection object that is provided by the client in the <b>pEvents</b> member of the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer">MFT_OUTPUT_DATA_BUFFER</a> structure, when the client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.
      

Events must be serialized with the samples that come before and after them. Attach the event to the output sample that follows the event. (The pipeline will process the event first, and then the sample.) If an MFT holds back one or more samples between calls to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a> and <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, the MFT should handle sending all events downstream, because in this situation the pipeline cannot correlate input samples with output samples.
      

If an MFT does not hold back samples and does not need to examine any events, it can return <b>E_NOTIMPL</b>.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTProcessEvent</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>