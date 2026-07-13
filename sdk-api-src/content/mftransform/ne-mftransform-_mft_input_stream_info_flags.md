---
UID: NE:mftransform._MFT_INPUT_STREAM_INFO_FLAGS
title: _MFT_INPUT_STREAM_INFO_FLAGS (mftransform.h)
description: Describes an input stream on a Media Foundation transform (MFT).
helpviewer_keywords: ["MFT_INPUT_STREAM_DOES_NOT_ADDREF","MFT_INPUT_STREAM_FIXED_SAMPLE_SIZE","MFT_INPUT_STREAM_HOLDS_BUFFERS","MFT_INPUT_STREAM_OPTIONAL","MFT_INPUT_STREAM_PROCESSES_IN_PLACE","MFT_INPUT_STREAM_REMOVABLE","MFT_INPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER","MFT_INPUT_STREAM_WHOLE_SAMPLES","_MFT_INPUT_STREAM_INFO_FLAGS","_MFT_INPUT_STREAM_INFO_FLAGS enumeration [Media Foundation]","d9a05a0f-56a7-4a91-93dc-a5079e51deac","mf._mft_input_stream_info_flags","mftransform/MFT_INPUT_STREAM_DOES_NOT_ADDREF","mftransform/MFT_INPUT_STREAM_FIXED_SAMPLE_SIZE","mftransform/MFT_INPUT_STREAM_HOLDS_BUFFERS","mftransform/MFT_INPUT_STREAM_OPTIONAL","mftransform/MFT_INPUT_STREAM_PROCESSES_IN_PLACE","mftransform/MFT_INPUT_STREAM_REMOVABLE","mftransform/MFT_INPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER","mftransform/MFT_INPUT_STREAM_WHOLE_SAMPLES","mftransform/_MFT_INPUT_STREAM_INFO_FLAGS"]
old-location: mf\_mft_input_stream_info_flags.htm
tech.root: mf
ms.assetid: d9a05a0f-56a7-4a91-93dc-a5079e51deac
ms.date: 12/05/2018
ms.keywords: MFT_INPUT_STREAM_DOES_NOT_ADDREF, MFT_INPUT_STREAM_FIXED_SAMPLE_SIZE, MFT_INPUT_STREAM_HOLDS_BUFFERS, MFT_INPUT_STREAM_OPTIONAL, MFT_INPUT_STREAM_PROCESSES_IN_PLACE, MFT_INPUT_STREAM_REMOVABLE, MFT_INPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER, MFT_INPUT_STREAM_WHOLE_SAMPLES, _MFT_INPUT_STREAM_INFO_FLAGS, _MFT_INPUT_STREAM_INFO_FLAGS enumeration [Media Foundation], d9a05a0f-56a7-4a91-93dc-a5079e51deac, mf._mft_input_stream_info_flags, mftransform/MFT_INPUT_STREAM_DOES_NOT_ADDREF, mftransform/MFT_INPUT_STREAM_FIXED_SAMPLE_SIZE, mftransform/MFT_INPUT_STREAM_HOLDS_BUFFERS, mftransform/MFT_INPUT_STREAM_OPTIONAL, mftransform/MFT_INPUT_STREAM_PROCESSES_IN_PLACE, mftransform/MFT_INPUT_STREAM_REMOVABLE, mftransform/MFT_INPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER, mftransform/MFT_INPUT_STREAM_WHOLE_SAMPLES, mftransform/_MFT_INPUT_STREAM_INFO_FLAGS
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_INPUT_STREAM_INFO_FLAGS
 - mftransform/_MFT_INPUT_STREAM_INFO_FLAGS
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
 - _MFT_INPUT_STREAM_INFO_FLAGS
---

# _MFT_INPUT_STREAM_INFO_FLAGS enumeration


## -description

Describes an input stream on a Media Foundation transform (MFT).

## -enum-fields

### -field MFT_INPUT_STREAM_WHOLE_SAMPLES:0x1

Each media sample (<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface) of input data must contain complete, unbroken units of data. The definition of a <i>unit of data</i> depends on the media type: For uncompressed video, a video frame; for compressed data, a compressed packet; for uncompressed audio, a single audio frame.

For uncompressed audio formats, this flag is always implied. (It is valid to set the flag, but not required.) An uncompressed audio frame should never span more than one media sample.

### -field MFT_INPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER:0x2

Each media sample that the client provides as input must contain exactly one unit of data, as defined for the MFT_INPUT_STREAM_WHOLE_SAMPLES flag.

If this flag is present, the MFT_INPUT_STREAM_WHOLE_SAMPLES flag must also be present.

An MFT that processes uncompressed audio should not set this flag. The MFT should accept buffers that contain more than a single audio frame, for efficiency.

### -field MFT_INPUT_STREAM_FIXED_SAMPLE_SIZE:0x4

All input samples must be the same size.
          The size is given in the <b>cbSize</b> member of the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_input_stream_info">MFT_INPUT_STREAM_INFO</a> structure. The MFT must provide this value. During processing, the MFT should verify the size of input samples, and may drop samples with incorrect size.

### -field MFT_INPUT_STREAM_HOLDS_BUFFERS:0x8

The MFT might hold one or more input samples after <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> is called. If this flag is present, the <b>hnsMaxLatency</b> member of the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_input_stream_info">MFT_INPUT_STREAM_INFO</a> structure gives the maximum latency, and the <b>cbMaxLookahead</b> member gives the maximum number of bytes of lookahead.

### -field MFT_INPUT_STREAM_DOES_NOT_ADDREF:0x100

The MFT does not hold input samples after the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a> method returns. It releases the sample before the <b>ProcessInput</b> method returns.

If this flag is absent, the MFT might hold a reference count on the samples that are passed to the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a> method. The client must not re-use or delete the buffer memory until the MFT releases the sample's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> pointer.

If this flag is absent, it does not guarantee that the MFT holds a reference count on the input samples. It is valid for an MFT to release input samples in <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a> even if the MFT does not set this flag. However, setting this flag might enable to client to optimize how it re-uses buffers.

An MFT should not set this flag if it ever holds onto an input sample after returning from <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a>.

### -field MFT_INPUT_STREAM_REMOVABLE:0x200

This input stream can be removed by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream">IMFTransform::DeleteInputStream</a>.

### -field MFT_INPUT_STREAM_OPTIONAL:0x400

This input stream is optional. The transform can produce output without receiving input from this stream. The caller can deselect the stream by not setting a media type or by setting a <b>NULL</b> media type. It is possible for every input stream on a transform to be optional, but at least one input must be selected in order to produce output.

### -field MFT_INPUT_STREAM_PROCESSES_IN_PLACE:0x800

The MFT can perform in-place processing. In this mode, the MFT directly modifies the input buffer. When the client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, the same sample that was delivered to this stream is returned in the output stream that has a matching stream identifier. This flag implies that the MFT holds onto the input buffer, so this flag cannot combined with the MFT_INPUT_STREAM_DOES_NOT_ADDREF flag.

If this flag is present, the MFT must set the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES or MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES flag for the output stream that corresponds to this input stream. (See <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a>).

## -remarks

Before the client sets the media types on the transform, the only flags guaranteed to be accurate are the MFT_INPUT_STREAM_REMOVABLE and MFT_INPUT_STREAM_OPTIONAL flags. For all other flags, the client should first set the media type on every non-optional stream.

In the default processing model, an MFT holds a reference count on the sample that it receives in <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a>. It does not process the sample immediately inside <b>ProcessInput</b>. When <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> is called, the MFT produces output data and then discards the input sample. The following variations on this model are defined:

<ul>
<li>
If an MFT never holds onto input samples between <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a> and <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, it can set the MFT_INPUT_STREAM_DOES_NOT_ADDREF.

</li>
<li>
If an MFT holds some input samples beyond the next call to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>, it can set the MFT_INPUT_STREAM_HOLDS_BUFFERS.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mftransform/ns-mftransform-mft_input_stream_info">MFT_INPUT_STREAM_INFO</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
