---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

