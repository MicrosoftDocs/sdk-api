---
UID: NE:mftransform._MFT_OUTPUT_STREAM_INFO_FLAGS
title: "_MFT_OUTPUT_STREAM_INFO_FLAGS"
author: windows-sdk-content
description: Describes an output stream on a Media Foundation transform (MFT).
old-location: mf\_mft_output_stream_info_flags.htm
old-project: medfound
ms.assetid: f67e1e81-baf5-414a-ac23-45d4d6317255
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES, MFT_OUTPUT_STREAM_DISCARDABLE, MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE, MFT_OUTPUT_STREAM_LAZY_READ, MFT_OUTPUT_STREAM_OPTIONAL, MFT_OUTPUT_STREAM_PROVIDES_SAMPLES, MFT_OUTPUT_STREAM_REMOVABLE, MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER, MFT_OUTPUT_STREAM_WHOLE_SAMPLES, _MFT_OUTPUT_STREAM_INFO_FLAGS, _MFT_OUTPUT_STREAM_INFO_FLAGS enumeration [Media Foundation], f67e1e81-baf5-414a-ac23-45d4d6317255, mf._mft_output_stream_info_flags, mftransform/MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES, mftransform/MFT_OUTPUT_STREAM_DISCARDABLE, mftransform/MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE, mftransform/MFT_OUTPUT_STREAM_LAZY_READ, mftransform/MFT_OUTPUT_STREAM_OPTIONAL, mftransform/MFT_OUTPUT_STREAM_PROVIDES_SAMPLES, mftransform/MFT_OUTPUT_STREAM_REMOVABLE, mftransform/MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER, mftransform/MFT_OUTPUT_STREAM_WHOLE_SAMPLES, mftransform/_MFT_OUTPUT_STREAM_INFO_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - _MFT_OUTPUT_STREAM_INFO_FLAGS
product: Windows
targetos: Windows
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFT_OUTPUT_STREAM_INFO_FLAGS enumeration


## -description



Describes an output stream on a Media Foundation transform (MFT).




## -enum-fields




### -field MFT_OUTPUT_STREAM_WHOLE_SAMPLES

Each media sample (<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface) of output data from the MFT contains complete, unbroken units of data. The definition of a <i>unit of data</i> depends on the media type: For uncompressed video, a video frame; for compressed data, a compressed packet; for uncompressed audio, a single audio frame.

For uncompressed audio formats, this flag is always implied. (It is valid to set the flag, but not required.) An uncompressed audio frame should never span more than one media sample.


### -field MFT_OUTPUT_STREAM_SINGLE_SAMPLE_PER_BUFFER

Each output sample contains exactly one unit of data, as defined for the MFT_OUTPUT_STREAM_WHOLE_SAMPLES flag.

If this flag is present, the MFT_OUTPUT_STREAM_WHOLE_SAMPLES flag must also be present.

An MFT that outputs uncompressed audio should not set this flag. For efficiency, it should output more than one audio frame at a time.


### -field MFT_OUTPUT_STREAM_FIXED_SAMPLE_SIZE

All output samples are the same size.


### -field MFT_OUTPUT_STREAM_DISCARDABLE

The MFT can discard the output data from this output stream, if requested by the client. To discard the output, set the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag in the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> method.


### -field MFT_OUTPUT_STREAM_OPTIONAL

This output stream is optional. The client can deselect the stream by not setting a media type or by setting a <b>NULL</b> media type. When an optional stream is deselected, it does not produce any output data.


### -field MFT_OUTPUT_STREAM_PROVIDES_SAMPLES

The MFT provides the output samples for this stream, either by allocating them internally or by operating directly on the input samples. The MFT cannot use output samples provided by the client for this stream.

If this flag is not set, the MFT must set <b>cbSize</b> to a nonzero value in the <a href="https://msdn.microsoft.com/4181d8b8-7c1b-4f8e-a0c6-63ab039539f6">MFT_OUTPUT_STREAM_INFO</a> structure, so that the client can allocate the correct buffer size. For more information, see <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a>. This flag cannot be combined with the MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES flag.


### -field MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES

The MFT can either provide output samples for this stream or it can use samples that the client allocates. This flag cannot be combined with the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag.

If the MFT does not set this flag or the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag, the client must allocate the samples for this output stream. The MFT will not provide its own samples.


### -field MFT_OUTPUT_STREAM_LAZY_READ

The MFT does not require the client to process the output for this stream. If the client continues to send input data without getting the output from this stream, the MFT simply discards the previous input.


### -field MFT_OUTPUT_STREAM_REMOVABLE

The MFT might remove this output stream during streaming. This flag typically applies to demultiplexers, where the input data contains multiple streams that can start and stop during streaming. For more information, see <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>.


## -remarks



Before the client sets the media types on the MFT, the only flag guaranteed to be accurate is the MFT_OUTPUT_STREAM_OPTIONAL flag. For all other flags, the client should first set the media type on every non-optional stream.

The MFT_OUTPUT_STREAM_DISCARDABLE and MFT_OUTPUT_STREAM_LAZY_READ flags define different behaviors for how the MFT can discard output data.

<ul>
<li>
MFT_OUTPUT_STREAM_DISCARDABLE: The MFT discards output data only if the client calls <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> with the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag. The MFT never discards data when the client calls <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">ProcessInput</a>.

</li>
<li>
MFT_OUTPUT_STREAM_LAZY_READ: If the client continues to call <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">ProcessInput</a> without collecting the output from this stream, the MFT eventually discards the output. If all output streams have the MFT_OUTPUT_STREAM_LAZY_READ flag, the MFT never refuses more input data.

</li>
</ul>
If neither of these flags is set, the MFT never discards output data.




## -see-also




<a href="https://msdn.microsoft.com/4181d8b8-7c1b-4f8e-a0c6-63ab039539f6">MFT_OUTPUT_STREAM_INFO</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

