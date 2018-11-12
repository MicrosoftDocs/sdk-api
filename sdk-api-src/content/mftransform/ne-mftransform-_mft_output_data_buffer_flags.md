---
UID: NE:mftransform._MFT_OUTPUT_DATA_BUFFER_FLAGS
title: "_MFT_OUTPUT_DATA_BUFFER_FLAGS"
author: windows-sdk-content
description: Defines flags for the IMFTransform::ProcessOutput method.
old-location: mf\_mft_output_data_buffer_flags.htm
tech.root: medfound
ms.assetid: b975a1a9-2cd1-4187-9934-c6877f10cec6
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE, MFT_OUTPUT_DATA_BUFFER_INCOMPLETE, MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE, MFT_OUTPUT_DATA_BUFFER_STREAM_END, _MFT_OUTPUT_DATA_BUFFER_FLAGS, _MFT_OUTPUT_DATA_BUFFER_FLAGS enumeration [Media Foundation], b975a1a9-2cd1-4187-9934-c6877f10cec6, mf._mft_output_data_buffer_flags, mftransform/MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE, mftransform/MFT_OUTPUT_DATA_BUFFER_INCOMPLETE, mftransform/MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE, mftransform/MFT_OUTPUT_DATA_BUFFER_STREAM_END, mftransform/_MFT_OUTPUT_DATA_BUFFER_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - _MFT_OUTPUT_DATA_BUFFER_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _MFT_OUTPUT_DATA_BUFFER_FLAGS enumeration


## -description


Defines flags for the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> method.
        


## -enum-fields




### -field MFT_OUTPUT_DATA_BUFFER_INCOMPLETE

The MFT can still generate output from this stream without receiving any more input. Call <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> again to process the next batch of input data.


### -field MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE

The format has changed on this output stream, or there is a new preferred format for this stream. When this flag is set, the MFT clears the media type for the stream. The <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method returns MF_E_TRANSFORM_STREAM_CHANGE and generates no output for any stream. Further calls to <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">IMFTransform::ProcessInput</a> or <b>ProcessOutput</b> will fail until the client sets a new media type.


### -field MFT_OUTPUT_DATA_BUFFER_STREAM_END

The MFT has removed this output stream. The output stream must have the MFT_OUTPUT_STREAM_REMOVABLE flag. (See <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a>.)

When the MFT removes an output stream, the MFT returns this status code on the next call to <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> after the last output sample has been produced. When the MFT returns this status code, it does not modify any sample contained in the <b>pSample</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure, nor does it allocate a new sample if <b>pSample</b> is <b>NULL</b>.

After this status code is returned, the stream identifier for this output stream is no longer valid. The client should no longer provide an <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure for that stream when it calls <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>.

The <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method does not return <b>MF_E_TRANSFORM_STREAM_CHANGE</b> when a stream ends, unless there is a change in another stream that requires this return code.


### -field MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE

There is no sample ready for this stream. This flag might be set if the MFT has multiple output streams that produce data at different times. It sets this flag for each stream that is not ready to produce data. It does not modify the output sample contained in the <b>pSample</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure, nor does it allocate a new sample is <b>pSample</b> is <b>NULL</b>.

If no streams are ready to produce output, the MFT does not set this flag. Instead, the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method returns MF_E_TRANSFORM_NEED_MORE_INPUT.


## -remarks



The values in this enumeration are not bit flags, so they should not be combined with a bitwise <b>OR</b>. Also, the caller should test for these flags with the equality operator, not a bitwise <b>AND</b>:

<pre class="syntax" xml:space="preserve"><code>// Correct.
if (Buffer.dwStatus == MFT_OUTPUT_DATA_BUFFER_STREAM_END)
{
    ...
}

// Incorrect.
if ((Buffer.dwStatus &amp; MFT_OUTPUT_DATA_BUFFER_STREAM_END) != 0)
{
    ...
}
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

