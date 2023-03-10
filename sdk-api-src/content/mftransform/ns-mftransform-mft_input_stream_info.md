---
UID: NS:mftransform._MFT_INPUT_STREAM_INFO
title: MFT_INPUT_STREAM_INFO (mftransform.h)
description: Contains information about an input stream on a Media Foundation transform (MFT). To get these values, call IMFTransform::GetInputStreamInfo.
helpviewer_keywords: ["MFT_INPUT_STREAM_INFO","MFT_INPUT_STREAM_INFO structure [Media Foundation]","de3d6d70-3525-42a0-bc1a-2625e7ebd918","mf.mft_input_stream_info","mftransform/MFT_INPUT_STREAM_INFO"]
old-location: mf\mft_input_stream_info.htm
tech.root: mf
ms.assetid: de3d6d70-3525-42a0-bc1a-2625e7ebd918
ms.date: 12/05/2018
ms.keywords: MFT_INPUT_STREAM_INFO, MFT_INPUT_STREAM_INFO structure [Media Foundation], de3d6d70-3525-42a0-bc1a-2625e7ebd918, mf.mft_input_stream_info, mftransform/MFT_INPUT_STREAM_INFO
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
req.typenames: MFT_INPUT_STREAM_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_INPUT_STREAM_INFO
 - mftransform/_MFT_INPUT_STREAM_INFO
 - MFT_INPUT_STREAM_INFO
 - mftransform/MFT_INPUT_STREAM_INFO
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
 - MFT_INPUT_STREAM_INFO
---

# MFT_INPUT_STREAM_INFO structure


## -description

Contains information about an input stream on a Media Foundation transform (MFT). To get these values, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo">IMFTransform::GetInputStreamInfo</a>.

## -struct-fields

### -field hnsMaxLatency

Maximum amount of time between an input sample and the corresponding output sample, in 100-nanosecond units. For example, an MFT that buffers two samples, each with a duration of 1 second, has a maximum latency of two seconds. If the MFT always turns input samples directly into output samples, with no buffering, the latency is zero.

### -field dwFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags">_MFT_INPUT_STREAM_INFO_FLAGS</a> enumeration.

### -field cbSize

The minimum size of each input buffer, in bytes. If the size is variable or the MFT does not require a specific size, the value is zero. For uncompressed audio, the value should be the audio frame size, which you can get from the <a href="/windows/desktop/medfound/mf-mt-audio-block-alignment-attribute">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> attribute in the media type.

### -field cbMaxLookahead

Maximum amount of input data, in bytes, that the MFT holds to perform lookahead. <i>Lookahead</i> is the action of looking forward in the data before processing it. This value should be the worst-case value. If the MFT does not keep a lookahead buffer, the value is zero.

### -field cbAlignment

The memory alignment required for input buffers. If the MFT does not require a specific alignment, the value is zero.

## -remarks

Before the media types are set, the only values that should be considered valid are the MFT_INPUT_STREAM_REMOVABLE and MFT_INPUT_STREAM_OPTIONAL flags in the <b>dwFlags</b> member.

<ul>
<li>
The MFT_INPUT_STREAM_REMOVABLE flag indicates that the stream can be deleted.

</li>
<li>
The MFT_INPUT_STREAM_OPTIONAL flag indicates that the stream is optional and does not require a media type.

</li>
</ul>
After you set a media type on all of the input and output streams (not including optional streams), all of the values returned by the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo">GetInputStreamInfo</a> method are valid. They might change if you set different media types.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>