---
UID: NE:mftransform._MFT_OUTPUT_STREAM_INFO_FLAGS
title: _MFT_OUTPUT_STREAM_INFO_FLAGS (mftransform.h)
description: Describes an output stream on a Media Foundation transform (MFT).
helpviewer_keywords: ["MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES","MFT_OUTPUT_STREAM_DISCARDABLE","MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE","MFT_OUTPUT_STREAM_LAZY_READ","MFT_OUTPUT_STREAM_OPTIONAL","MFT_OUTPUT_STREAM_PROVIDES_SAMPLES","MFT_OUTPUT_STREAM_REMOVABLE","MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER","MFT_OUTPUT_STREAM_WHOLE_SAMPLES","_MFT_OUTPUT_STREAM_INFO_FLAGS","_MFT_OUTPUT_STREAM_INFO_FLAGS enumeration [Media Foundation]","f67e1e81-baf5-414a-ac23-45d4d6317255","mf._mft_output_stream_info_flags","mftransform/MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES","mftransform/MFT_OUTPUT_STREAM_DISCARDABLE","mftransform/MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE","mftransform/MFT_OUTPUT_STREAM_LAZY_READ","mftransform/MFT_OUTPUT_STREAM_OPTIONAL","mftransform/MFT_OUTPUT_STREAM_PROVIDES_SAMPLES","mftransform/MFT_OUTPUT_STREAM_REMOVABLE","mftransform/MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER","mftransform/MFT_OUTPUT_STREAM_WHOLE_SAMPLES","mftransform/_MFT_OUTPUT_STREAM_INFO_FLAGS"]
old-location: mf\_mft_output_stream_info_flags.htm
tech.root: mf
ms.assetid: f67e1e81-baf5-414a-ac23-45d4d6317255
ms.date: 12/05/2018
ms.keywords: MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES, MFT_OUTPUT_STREAM_DISCARDABLE, MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE, MFT_OUTPUT_STREAM_LAZY_READ, MFT_OUTPUT_STREAM_OPTIONAL, MFT_OUTPUT_STREAM_PROVIDES_SAMPLES, MFT_OUTPUT_STREAM_REMOVABLE, MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER, MFT_OUTPUT_STREAM_WHOLE_SAMPLES, _MFT_OUTPUT_STREAM_INFO_FLAGS, _MFT_OUTPUT_STREAM_INFO_FLAGS enumeration [Media Foundation], f67e1e81-baf5-414a-ac23-45d4d6317255, mf._mft_output_stream_info_flags, mftransform/MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES, mftransform/MFT_OUTPUT_STREAM_DISCARDABLE, mftransform/MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE, mftransform/MFT_OUTPUT_STREAM_LAZY_READ, mftransform/MFT_OUTPUT_STREAM_OPTIONAL, mftransform/MFT_OUTPUT_STREAM_PROVIDES_SAMPLES, mftransform/MFT_OUTPUT_STREAM_REMOVABLE, mftransform/MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER, mftransform/MFT_OUTPUT_STREAM_WHOLE_SAMPLES, mftransform/_MFT_OUTPUT_STREAM_INFO_FLAGS
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
 - _MFT_OUTPUT_STREAM_INFO_FLAGS
 - mftransform/_MFT_OUTPUT_STREAM_INFO_FLAGS
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
 - _MFT_OUTPUT_STREAM_INFO_FLAGS
---

# _MFT_OUTPUT_STREAM_INFO_FLAGS enumeration


## -description

Describes an output stream on a Media Foundation transform (MFT).

## -enum-fields

### -field MFT_OUTPUT_STREAM_WHOLE_SAMPLES:0x1

Each media sample (<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface) of output data from the MFT contains complete, unbroken units of data. The definition of a <i>unit of data</i> depends on the media type: For uncompressed video, a video frame; for compressed data, a compressed packet; for uncompressed audio, a single audio frame.

For uncompressed audio formats, this flag is always implied. (It is valid to set the flag, but not required.) An uncompressed audio frame should never span more than one media sample.

### -field MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER:0x2

Each output sample contains exactly one unit of data, as defined for the MFT_OUTPUT_STREAM_WHOLE_SAMPLES flag.

If this flag is present, the MFT_OUTPUT_STREAM_WHOLE_SAMPLES flag must also be present.

An MFT that outputs uncompressed audio should not set this flag. For efficiency, it should output more than one audio frame at a time.

### -field MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE:0x4

All output samples are the same size.

### -field MFT_OUTPUT_STREAM_DISCARDABLE:0x8

The MFT can discard the output data from this output stream, if requested by the client. To discard the output, set the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag in the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> method.

### -field MFT_OUTPUT_STREAM_OPTIONAL:0x10

This output stream is optional. The client can deselect the stream by not setting a media type or by setting a <b>NULL</b> media type. When an optional stream is deselected, it does not produce any output data.

### -field MFT_OUTPUT_STREAM_PROVIDES_SAMPLES:0x100

The MFT provides the output samples for this stream, either by allocating them internally or by operating directly on the input samples. The MFT cannot use output samples provided by the client for this stream.

If this flag is not set, the MFT must set <b>cbSize</b> to a nonzero value in the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info">MFT_OUTPUT_STREAM_INFO</a> structure, so that the client can allocate the correct buffer size. For more information, see <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a>. This flag cannot be combined with the MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES flag.

### -field MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES:0x200

The MFT can either provide output samples for this stream or it can use samples that the client allocates. This flag cannot be combined with the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag.

If the MFT does not set this flag or the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag, the client must allocate the samples for this output stream. The MFT will not provide its own samples.

### -field MFT_OUTPUT_STREAM_LAZY_READ:0x400

The MFT does not require the client to process the output for this stream. If the client continues to send input data without getting the output from this stream, the MFT simply discards the previous input.

### -field MFT_OUTPUT_STREAM_REMOVABLE:0x800

The MFT might remove this output stream during streaming. This flag typically applies to demultiplexers, where the input data contains multiple streams that can start and stop during streaming. For more information, see <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.

## -remarks

Before the client sets the media types on the MFT, the only flag guaranteed to be accurate is the MFT_OUTPUT_STREAM_OPTIONAL flag. For all other flags, the client should first set the media type on every non-optional stream.

The MFT_OUTPUT_STREAM_DISCARDABLE and MFT_OUTPUT_STREAM_LAZY_READ flags define different behaviors for how the MFT can discard output data.

<ul>
<li>
MFT_OUTPUT_STREAM_DISCARDABLE: The MFT discards output data only if the client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> with the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag. The MFT never discards data when the client calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a>.

</li>
<li>
MFT_OUTPUT_STREAM_LAZY_READ: If the client continues to call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a> without collecting the output from this stream, the MFT eventually discards the output. If all output streams have the MFT_OUTPUT_STREAM_LAZY_READ flag, the MFT never refuses more input data.

</li>
</ul>
If neither of these flags is set, the MFT never discards output data.

## -see-also

<a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info">MFT_OUTPUT_STREAM_INFO</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
