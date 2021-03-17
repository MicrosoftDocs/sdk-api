---
UID: NS:mftransform._MFT_OUTPUT_STREAM_INFO
title: MFT_OUTPUT_STREAM_INFO (mftransform.h)
description: Contains information about an output stream on a Media Foundation transform (MFT). To get these values, call IMFTransform::GetOutputStreamInfo.
helpviewer_keywords: ["4181d8b8-7c1b-4f8e-a0c6-63ab039539f6","MFT_OUTPUT_STREAM_INFO","MFT_OUTPUT_STREAM_INFO structure [Media Foundation]","mf.mft_output_stream_info","mftransform/MFT_OUTPUT_STREAM_INFO"]
old-location: mf\mft_output_stream_info.htm
tech.root: mf
ms.assetid: 4181d8b8-7c1b-4f8e-a0c6-63ab039539f6
ms.date: 12/05/2018
ms.keywords: 4181d8b8-7c1b-4f8e-a0c6-63ab039539f6, MFT_OUTPUT_STREAM_INFO, MFT_OUTPUT_STREAM_INFO structure [Media Foundation], mf.mft_output_stream_info, mftransform/MFT_OUTPUT_STREAM_INFO
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
req.typenames: MFT_OUTPUT_STREAM_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_OUTPUT_STREAM_INFO
 - mftransform/_MFT_OUTPUT_STREAM_INFO
 - MFT_OUTPUT_STREAM_INFO
 - mftransform/MFT_OUTPUT_STREAM_INFO
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
 - MFT_OUTPUT_STREAM_INFO
---

# MFT_OUTPUT_STREAM_INFO structure


## -description

Contains information about an output stream on a Media Foundation transform (MFT). To get these values, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">IMFTransform::GetOutputStreamInfo</a>.

## -struct-fields

### -field dwFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags">_MFT_OUTPUT_STREAM_INFO_FLAGS</a> enumeration.

### -field cbSize

Minimum size of each output buffer, in bytes. If the MFT does not require a specific size, the value is zero. For uncompressed audio, the value should be the audio frame size, which you can get from the <a href="/windows/desktop/medfound/mf-mt-audio-block-alignment-attribute">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> attribute in the media type.

If the <b>dwFlags</b> member contains the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag, the value is zero, because the MFT allocates the output buffers.

### -field cbAlignment

The memory alignment required for output buffers. If the MFT does not require a specific alignment, the value is zero. If the <b>dwFlags</b> member contains the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag, this value is the alignment that the MFT uses internally when it allocates samples. It is recommended, but not required, that MFTs allocate buffers with at least a 16-byte memory alignment.

## -remarks

Before the media types are set, the only values that should be considered valid is the MFT_OUTPUT_STREAM_OPTIONAL flag in the <b>dwFlags</b> member. This flag indicates that the stream is optional and does not require a media type.

After you set a media type on all of the input and output streams (not including optional streams), all of the values returned by the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo">GetOutputStreamInfo</a> method are valid. They might change if you set different media types.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>