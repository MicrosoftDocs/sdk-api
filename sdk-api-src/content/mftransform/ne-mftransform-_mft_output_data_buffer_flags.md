---
UID: NE:mftransform._MFT_OUTPUT_DATA_BUFFER_FLAGS
title: _MFT_OUTPUT_DATA_BUFFER_FLAGS (mftransform.h)
description: Defines flags for the IMFTransform::ProcessOutput method.
helpviewer_keywords: ["MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE","MFT_OUTPUT_DATA_BUFFER_INCOMPLETE","MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE","MFT_OUTPUT_DATA_BUFFER_STREAM_END","_MFT_OUTPUT_DATA_BUFFER_FLAGS","_MFT_OUTPUT_DATA_BUFFER_FLAGS enumeration [Media Foundation]","b975a1a9-2cd1-4187-9934-c6877f10cec6","mf._mft_output_data_buffer_flags","mftransform/MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE","mftransform/MFT_OUTPUT_DATA_BUFFER_INCOMPLETE","mftransform/MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE","mftransform/MFT_OUTPUT_DATA_BUFFER_STREAM_END","mftransform/_MFT_OUTPUT_DATA_BUFFER_FLAGS"]
old-location: mf\_mft_output_data_buffer_flags.htm
tech.root: mf
ms.assetid: b975a1a9-2cd1-4187-9934-c6877f10cec6
ms.date: 12/05/2018
ms.keywords: MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE, MFT_OUTPUT_DATA_BUFFER_INCOMPLETE, MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE, MFT_OUTPUT_DATA_BUFFER_STREAM_END, _MFT_OUTPUT_DATA_BUFFER_FLAGS, _MFT_OUTPUT_DATA_BUFFER_FLAGS enumeration [Media Foundation], b975a1a9-2cd1-4187-9934-c6877f10cec6, mf._mft_output_data_buffer_flags, mftransform/MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE, mftransform/MFT_OUTPUT_DATA_BUFFER_INCOMPLETE, mftransform/MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE, mftransform/MFT_OUTPUT_DATA_BUFFER_STREAM_END, mftransform/_MFT_OUTPUT_DATA_BUFFER_FLAGS
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
 - _MFT_OUTPUT_DATA_BUFFER_FLAGS
 - mftransform/_MFT_OUTPUT_DATA_BUFFER_FLAGS
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
 - _MFT_OUTPUT_DATA_BUFFER_FLAGS
---

# _MFT_OUTPUT_DATA_BUFFER_FLAGS enumeration


## -description

Defines flags for the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> method.

## -enum-fields

### -field MFT_OUTPUT_DATA_BUFFER_INCOMPLETE:0x1000000

The MFT can still generate output from this stream without receiving any more input. Call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> again to process the next batch of input data.

### -field MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE:0x100

The format has changed on this output stream, or there is a new preferred format for this stream. When this flag is set, the MFT clears the media type for the stream. The <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> method returns MF_E_TRANSFORM_STREAM_CHANGE and generates no output for any stream. Further calls to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a> or <b>ProcessOutput</b> will fail until the client sets a new media type.

### -field MFT_OUTPUT_DATA_BUFFER_STREAM_END:0x200

The MFT has removed this output stream. The output stream must have the MFT_OUTPUT_STREAM_REMOVABLE flag. (See <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a>.)

When the MFT removes an output stream, the MFT returns this status code on the next call to <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> after the last output sample has been produced. When the MFT returns this status code, it does not modify any sample contained in the <b>pSample</b> member of the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer">MFT_OUTPUT_DATA_BUFFER</a> structure, nor does it allocate a new sample if <b>pSample</b> is <b>NULL</b>.

After this status code is returned, the stream identifier for this output stream is no longer valid. The client should no longer provide an <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer">MFT_OUTPUT_DATA_BUFFER</a> structure for that stream when it calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>.

The <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> method does not return <b>MF_E_TRANSFORM_STREAM_CHANGE</b> when a stream ends, unless there is a change in another stream that requires this return code.

### -field MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE:0x300

There is no sample ready for this stream. This flag might be set if the MFT has multiple output streams that produce data at different times. It sets this flag for each stream that is not ready to produce data. It does not modify the output sample contained in the <b>pSample</b> member of the <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer">MFT_OUTPUT_DATA_BUFFER</a> structure, nor does it allocate a new sample is <b>pSample</b> is <b>NULL</b>.

If no streams are ready to produce output, the MFT does not set this flag. Instead, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> method returns MF_E_TRANSFORM_NEED_MORE_INPUT.

## -remarks

The values in this enumeration are not bit flags, so they should not be combined with a bitwise <b>OR</b>. Also, the caller should test for these flags with the equality operator, not a bitwise <b>AND</b>:


``` syntax
// Correct.
if (Buffer.dwStatus == MFT_OUTPUT_DATA_BUFFER_STREAM_END)
{
    ...
}

// Incorrect.
if ((Buffer.dwStatus &amp; MFT_OUTPUT_DATA_BUFFER_STREAM_END) != 0)
{
    ...
}

```


## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
