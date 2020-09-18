---
UID: NS:mftransform._MFT_OUTPUT_DATA_BUFFER
title: MFT_OUTPUT_DATA_BUFFER (mftransform.h)
description: Contains information about an output buffer for a Media Foundation transform. This structure is used in the IMFTransform::ProcessOutput method.
helpviewer_keywords: ["*PMFT_OUTPUT_DATA_BUFFER","57623c8f-f7b6-4cb3-8d54-4ee516c706c3","MFT_OUTPUT_DATA_BUFFER","MFT_OUTPUT_DATA_BUFFER structure [Media Foundation]","mf.mft_output_data_buffer","mftransform/MFT_OUTPUT_DATA_BUFFER"]
old-location: mf\mft_output_data_buffer.htm
tech.root: mf
ms.assetid: 57623c8f-f7b6-4cb3-8d54-4ee516c706c3
ms.date: 12/05/2018
ms.keywords: '*PMFT_OUTPUT_DATA_BUFFER, 57623c8f-f7b6-4cb3-8d54-4ee516c706c3, MFT_OUTPUT_DATA_BUFFER, MFT_OUTPUT_DATA_BUFFER structure [Media Foundation], mf.mft_output_data_buffer, mftransform/MFT_OUTPUT_DATA_BUFFER'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFT_OUTPUT_DATA_BUFFER, *PMFT_OUTPUT_DATA_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_OUTPUT_DATA_BUFFER
 - mftransform/_MFT_OUTPUT_DATA_BUFFER
 - PMFT_OUTPUT_DATA_BUFFER
 - mftransform/PMFT_OUTPUT_DATA_BUFFER
 - MFT_OUTPUT_DATA_BUFFER
 - mftransform/MFT_OUTPUT_DATA_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - MFT_OUTPUT_DATA_BUFFER
---

# MFT_OUTPUT_DATA_BUFFER structure


## -description

Contains information about an output buffer for a Media Foundation transform. This structure is used in the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> method.

## -struct-fields

### -field dwStreamID

Output stream identifier. Before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, set this member to a valid stream identifier.

Exception: If the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a> method returns E_NOTIMPL, the MFT ignores this member and uses the indexes of the <i>pOutputSamples</i> array in the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> method as the stream identifiers. In other words, it uses the first element in the array for stream 0, the second for stream 1, and so forth. It is recommended (but not required) that the caller set <b>dwStreamID</b> equal to the array index in this case.

### -field pSample

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface. Before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, set this member equal to a valid <b>IMFSample</b> pointer or <b>NULL</b>. See Remarks for more information.

### -field dwStatus

Before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, set this member to zero. When the method returns, the MFT might set the member equal to a value from the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags">_MFT_OUTPUT_DATA_BUFFER_FLAGS</a> enumeration. Otherwise, the MFT leaves this member equal to zero.

### -field pEvents

Before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, set this member to <b>NULL</b>. On output, the MFT might set this member to a valid <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a> interface pointer. The pointer represents a collecton that contains zero or more events. To get each event, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement">IMFCollection::GetElement</a> and query the returned <b>IUnknown</b> pointer for the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface. When the <b>ProcessOutput</b> method returns, the caller is responsible for releasing the <b>IMFCollection</b> pointer if the pointer is not <b>NULL</b>.

## -remarks

You must provide an <b>MFT_OUTPUT_DATA_BUFFER</b> structure for each selected output stream.

MFTs can support two different allocation models for output samples:

<ul>
<li>The MFT allocates the output sample.
          </li>
<li>The client allocates the output sample.
          </li>
</ul>
To find which model the MFT supports for a given output stream, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a> and check the value of <b>dwFlags</b>.

<table>
<tr>
<th>Flag</th>
<th>Allocation Model</th>
</tr>
<tr>
<td>MFT_OUTPUT_STREAM_PROVIDES_SAMPLES</td>
<td>The MFT allocates the output samples for the stream. Set <b>pSample</b> to <b>NULL</b> for this stream.</td>
</tr>
<tr>
<td>MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES</td>
<td>The MFT supports both allocation models.</td>
</tr>
<tr>
<td>Neither (default)</td>
<td>The client must allocate the output samples for the stream.</td>
</tr>
</table>
 

The behavior of <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> depends on the initial value of <b>pSample</b> and the value of the <i>dwFlags</i> parameter in the <b>ProcessOutput</b> method.

<ul>
<li>
If <b>pSample</b> is <b>NULL</b> and <i>dwFlags</i> contains the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag, the MFT discards the output data.

Restriction: This output stream must have the MFT_OUTPUT_STREAM_DISCARDABLE or MFT_OUTPUT_STREAM_LAZY_READ flag. (To get the flags for the output stream, call the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a> method.)

</li>
<li>
If <b>pSample</b> is <b>NULL</b> and <i>dwFlags</i> does not contain the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, the MFT provides a sample for the output data. The MFT sets <b>pSample</b> to point to the sample that it provides. The MFT can either allocate a new sample or re-use an input sample.

Restriction: This output stream must have the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES or MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES flag.

</li>
<li>
If <b>pSample</b> is non-<b>NULL</b>, the MFT uses the sample provided by the caller.

Restriction: This output stream must not have the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag.

</li>
</ul>
Any other combinations are invalid and cause <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> to return E_INVALIDARG.

Each call to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> can produce zero or more events and up to one sample per output stream.

## -see-also

<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>