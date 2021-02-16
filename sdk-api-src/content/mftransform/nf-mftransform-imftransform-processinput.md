---
UID: NF:mftransform.IMFTransform.ProcessInput
title: IMFTransform::ProcessInput (mftransform.h)
description: Delivers data to an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["IMFTransform interface [Media Foundation]","ProcessInput method","IMFTransform.ProcessInput","IMFTransform::ProcessInput","ProcessInput","ProcessInput method [Media Foundation]","ProcessInput method [Media Foundation]","IMFTransform interface","c94d406b-7cd9-42d4-ae9e-3d21dbb47209","mf.imftransform_processinput","mftransform/IMFTransform::ProcessInput"]
old-location: mf\imftransform_processinput.htm
tech.root: mf
ms.assetid: c94d406b-7cd9-42d4-ae9e-3d21dbb47209
ms.date: 12/05/2018
ms.keywords: IMFTransform interface [Media Foundation],ProcessInput method, IMFTransform.ProcessInput, IMFTransform::ProcessInput, ProcessInput, ProcessInput method [Media Foundation], ProcessInput method [Media Foundation],IMFTransform interface, c94d406b-7cd9-42d4-ae9e-3d21dbb47209, mf.imftransform_processinput, mftransform/IMFTransform::ProcessInput
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
 - IMFTransform::ProcessInput
 - mftransform/IMFTransform::ProcessInput
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
 - IMFTransform.ProcessInput
---

# IMFTransform::ProcessInput


## -description

Delivers data to an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param pSample [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the input sample. The sample must contain at least one media buffer that contains valid input data.

### -param dwFlags [in]

Reserved. Must be zero.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_SAMPLE_DURATION</b></dt>
</dl>
</td>
<td width="60%">
The input sample requires a valid sample duration. To set the duration, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration">IMFSample::SetSampleDuration</a>. 

Some MFTs require that input samples have valid durations. Some MFTs do not require sample durations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_SAMPLE_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
The input sample requires a time stamp. To set the time stamp, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime">IMFSample::SetSampleTime</a>. 

Some MFTs require that input samples have valid time stamps. Some MFTs do not require time stamps.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The transform cannot process more input at this time.
              

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
<dt><b>MF_E_UNSUPPORTED_D3D_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The media type is not supported for DirectX Video Acceleration (DXVA). A DXVA-enabled decoder might return this error code.
              

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you are converting a DirectX Media Object (DMO) to an MFT, be aware that <b>S_FALSE</b> is not a valid return code for <b>IMFTransform::ProcessInput</b>, unlike the <b>IMediaObject::ProcessInput</b> method.</div>
<div> </div>

## -remarks

In most cases, if the method succeeds, the MFT stores the sample and holds a reference count on the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> pointer. Do not re-use the sample until the MFT releases the sample. Instead of storing the sample, however, an MFT might copy the sample data into a new buffer. In that case, the MFT should set the <b>MFT_INPUT_STREAM_DOES_NOT_ADDREF</b> flag in the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo">IMFTransform::GetInputStreamInfo</a> method.
      

If the MFT already has enough input data to produce an output sample, it does not accept new input data, and <b>ProcessInput</b> returns <b>MF_E_NOTACCEPTING</b>. At that point, the client should clear the pending input data by doing one of the following:
        

<ul>
<li>Generate new output by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.
          </li>
<li>Flush the input data by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">IMFTransform::ProcessMessage</a> with the MFT_<b>MESSAGE_COMMAND_FLUSH</b> message.
          </li>
</ul>
An exception to this rule is the <b>MFT_OUTPUT_STREAM_LAZY_READ</b> flag. When this flag is present, the transform will discard stored samples if you give it more input. For more information, see <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a>. A transform should never queue any more input data than is required to produce the correct output.
      

An MFT can process the input data in the <b>ProcessInput</b> method. However, most MFTs wait until the client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>.
      

After the client has set valid media types on all of the streams, the MFT should always be in one of two states: Able to accept more input, or able to produce more output. It should never be in both states or neither state. An MFT should only accept as much input as it needs to generate at least one output sample, at which point <b>ProcessInput</b> returns <b>MF_E_NOTACCEPTING</b>. When <b>ProcessInput</b> returns <b>MF_E_NOTACCEPTING</b>, the client can assume that the MFT is ready to produce output.
      

If an MFT encounters a non-fatal error in the input data, it can simply drop the data and attempt to recover when it gets the more input data. To request more input data, the MFT returns <b>MF_E_TRANSFORM_NEED_MORE_INPUT</b> from the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> method. If the MFT drops any data, it should set the <a href="/windows/desktop/medfound/mfsampleextension-discontinuity-attribute">MFSampleExtension_Discontinuity</a> attribute attribute on the next output sample, to notify the caller that there is a gap in the data stream.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTProcessInput</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Asynchronous_Processing"></a><a id="asynchronous_processing"></a><a id="ASYNCHRONOUS_PROCESSING"></a>Asynchronous Processing</h3>
The previous remarks describe the <i>synchronous</i> processing model. To support asynchronous processing, see <a href="/windows/desktop/medfound/asynchronous-mfts">Asynchronous MFTs</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>