---
UID: NS:mftransform._MFT_OUTPUT_DATA_BUFFER
title: MFT_OUTPUT_DATA_BUFFER (mftransform.h)
author: windows-sdk-content
description: Contains information about an output buffer for a Media Foundation transform. This structure is used in the IMFTransform::ProcessOutput method.
old-location: mf\mft_output_data_buffer.htm
tech.root: medfound
ms.assetid: 57623c8f-f7b6-4cb3-8d54-4ee516c706c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMFT_OUTPUT_DATA_BUFFER, 57623c8f-f7b6-4cb3-8d54-4ee516c706c3, MFT_OUTPUT_DATA_BUFFER, MFT_OUTPUT_DATA_BUFFER structure [Media Foundation], mf.mft_output_data_buffer, mftransform/MFT_OUTPUT_DATA_BUFFER"
ms.topic: struct
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
 - MFT_OUTPUT_DATA_BUFFER
product: Windows
targetos: Windows
req.typenames: MFT_OUTPUT_DATA_BUFFER, *PMFT_OUTPUT_DATA_BUFFER
req.redist: 
---

# MFT_OUTPUT_DATA_BUFFER structure


## -description



Contains information about an output buffer for a Media Foundation transform. This structure is used in the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> method.




## -struct-fields




### -field dwStreamID

Output stream identifier. Before calling <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>, set this member to a valid stream identifier.

Exception: If the <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a> method returns E_NOTIMPL, the MFT ignores this member and uses the indexes of the <i>pOutputSamples</i> array in the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method as the stream identifiers. In other words, it uses the first element in the array for stream 0, the second for stream 1, and so forth. It is recommended (but not required) that the caller set <b>dwStreamID</b> equal to the array index in this case.


### -field pSample

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface. Before calling <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>, set this member equal to a valid <b>IMFSample</b> pointer or <b>NULL</b>. See Remarks for more information.


### -field dwStatus

Before calling <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>, set this member to zero. When the method returns, the MFT might set the member equal to a value from the <a href="https://msdn.microsoft.com/b975a1a9-2cd1-4187-9934-c6877f10cec6">_MFT_OUTPUT_DATA_BUFFER_FLAGS</a> enumeration. Otherwise, the MFT leaves this member equal to zero.


### -field pEvents

Before calling <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>, set this member to <b>NULL</b>. On output, the MFT might set this member to a valid <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> interface pointer. The pointer represents a collecton that contains zero or more events. To get each event, call <a href="https://msdn.microsoft.com/a45983a8-4061-40e1-a11a-67de0867e553">IMFCollection::GetElement</a> and query the returned <b>IUnknown</b> pointer for the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface. When the <b>ProcessOutput</b> method returns, the caller is responsible for releasing the <b>IMFCollection</b> pointer if the pointer is not <b>NULL</b>.


## -remarks



You must provide an <b>MFT_OUTPUT_DATA_BUFFER</b> structure for each selected output stream.

MFTs can support two different allocation models for output samples:

<ul>
<li>The MFT allocates the output sample.
          </li>
<li>The client allocates the output sample.
          </li>
</ul>
To find which model the MFT supports for a given output stream, call <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a> and check the value of <b>dwFlags</b>.

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
 

The behavior of <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> depends on the initial value of <b>pSample</b> and the value of the <i>dwFlags</i> parameter in the <b>ProcessOutput</b> method.

<ul>
<li>
If <b>pSample</b> is <b>NULL</b> and <i>dwFlags</i> contains the MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag, the MFT discards the output data.

Restriction: This output stream must have the MFT_OUTPUT_STREAM_DISCARDABLE or MFT_OUTPUT_STREAM_LAZY_READ flag. (To get the flags for the output stream, call the <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a> method.)

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
Any other combinations are invalid and cause <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> to return E_INVALIDARG.

Each call to <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> can produce zero or more events and up to one sample per output stream.




## -see-also




<a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

