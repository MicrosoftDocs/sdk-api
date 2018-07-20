---
UID: NF:mftransform.IMFTransform.ProcessOutput
title: IMFTransform::ProcessOutput
author: windows-sdk-content
description: Generates output from the current input data.
old-location: mf\imftransform_processoutput.htm
old-project: medfound
ms.assetid: dc58cc75-7e01-4f47-a572-8e3ca1bc43b4
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFTransform interface [Media Foundation],ProcessOutput method, IMFTransform.ProcessOutput, IMFTransform::ProcessOutput, ProcessOutput, ProcessOutput method [Media Foundation], ProcessOutput method [Media Foundation],IMFTransform interface, dc58cc75-7e01-4f47-a572-8e3ca1bc43b4, mf.imftransform_processoutput, mftransform/IMFTransform::ProcessOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.ProcessOutput
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::ProcessOutput


## -description



          Generates output from the current input data.
        


## -parameters




### -param dwFlags [in]


            Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/846e91a5-7cd8-4b58-9484-b9cb9af0bebf">_MFT_PROCESS_OUTPUT_FLAGS</a> enumeration.
          


### -param cOutputBufferCount [in]


            Number of elements in the <i>pOutputSamples</i> array. The value must be at least 1.
          


### -param pOutputSamples [in, out]


            Pointer to an array of <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structures, allocated by the caller. The MFT uses this array to return output data to the caller.
          


### -param pdwStatus [out]


            Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/80804b33-1dac-41f8-8446-8f929bf9b931">_MFT_PROCESS_OUTPUT_STATUS</a> enumeration.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method was called on an asynchronous MFT that was not expecting this method call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">

                Invalid stream identifier in the <b>dwStreamID</b> member of one or more <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structures.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_NEED_MORE_INPUT</b></dt>
</dl>
</td>
<td width="60%">

                The transform cannot produce output data until it receives more input data.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_STREAM_CHANGE</b></dt>
</dl>
</td>
<td width="60%">

                The format has changed on an output stream, or there is a new preferred format, or there is a new output stream.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">

                You must set the media type on one or more streams of the MFT.
              

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you are converting a DirectX Media Object (DMO) to an MFT, be aware that <b>S_FALSE</b> is not a valid return code for <b>IMFTransform::ProcessOutput</b>, unlike the <b>IMediaObject::ProcessOutput</b> method.</div>
<div> </div>



## -remarks




        The size of the <i>pOutputSamples</i> array must be equal to or greater than the number of <i>selected</i> output streams. The number of selected output streams equals the total number of output streams minus the number of <i>deselected</i> streams. A stream is deselected if it has the <b>MFT_OUTPUT_STREAM_OPTIONAL</b> flag and the caller does not set a media type (or sets the media type to <b>NULL</b>). For more information, see <a href="https://msdn.microsoft.com/f67e1e81-baf5-414a-ac23-45d4d6317255">_MFT_OUTPUT_STREAM_INFO_FLAGS</a> enumeration.
      

This method generates output samples and can also generate events. If the method succeeds, at least one of the following conditions is true:

<ul>
<li>
            One or more samples in the <i>pOutputSamples</i> array contains output data.
          </li>
<li>
            One or more members of the <i>pOutputSamples</i> array contains a non-empty collection of events.
          </li>
</ul>
If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including Mftransform.h, this method is renamed <b>MFTProcessOutput</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Output_Buffers"></a><a id="output_buffers"></a><a id="OUTPUT_BUFFERS"></a>Output Buffers</h3>
The MFT returns output data for a stream through the <b>pSample</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure. This structure member is a pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of a media sample. (See <a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>.) The media sample is allocated either by the caller or by the MFT, depending on the MFT's allocation model. To find the allocation model, call <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a> and examine the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/4181d8b8-7c1b-4f8e-a0c6-63ab039539f6">MFT_OUTPUT_STREAM_INFO</a> structure:

<ul>
<li>
              If the <b>MFT_OUTPUT_STREAM_PROVIDES_SAMPLES</b> flag is present, the MFT allocates the media sample.
            </li>
<li>
              If the <b>MFT_OUTPUT_STREAM_CAN_PROVIDE_SAMPLES</b> flag is present, the caller can optionally provide a media sample. If <b>pSample</b> is <b>NULL</b>, the MFT will allocate the media sample.
            </li>
<li>
              If neither of these two flags is present, the caller must allocate the media sample.
            </li>
</ul>
These flags remain constant unless the media type for the output stream changes.

If the caller allocates the media sample, the media sample must contain a buffer that is large enough to hold the output data. To find the buffer requirements, call <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">GetOutputStreamInfo</a>. The MFT writes the output data to the start of the buffer, overwriting any data that already exists in the buffer.

If the MFT allocates the sample, the MFT also allocates the buffers for the sample.

If the MFT has multiple output streams, the streams might produce output at different rates, so some streams might have output while other streams do not. If a stream did not any produce output, the MFT sets the <b>MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE</b> flag in the <b>dwStatus</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure for that stream. In that case, if the caller allocated <b>pSample</b>, the buffers in the sample do not contain any valid data. If the caller did not allocate <b>pSample</b>, the <b>MFT_OUTPUT_DATA_BUFFER_NO_SAMPLE</b> flag indicates that <b>pSample</b> still equals <b>NULL</b> after the method returns.

If no output streams have data, and the MFT has no events to return, then <b>ProcessOutput</b> returns <b>MF_E_TRANSFORM_NEED_MORE_INPUT</b>.

The MFT cannot return more than one sample per stream in a single call to <b>ProcessOutput</b>. If there is more output data available for a stream after <b>ProcessOutput</b> returns, the MFT sets the <b>MFT_OUTPUT_DATA_BUFFER_INCOMPLETE</b> flag in the <b>dwStatus</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure for that stream.

If the MFT has enough data to produce output, it should refuse to accept any more input until <b>ProcessOutput</b> has been called enough times to pull all of the available output. (An exception is when the <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a> method returns the <b>MFT_OUTPUT_STREAM_LAZY_READ</b> flag.) Generally, an MFT with multiple output streams should produce output for a stream as soon as possible, and not wait for all of the streams to have output.

<h3><a id="In-Band_Events"></a><a id="in-band_events"></a><a id="IN-BAND_EVENTS"></a>In-Band Events</h3>
The MFT can return a collection of event objects in the <b>pEvents</b> member of each <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure. The MFT allocates both the collection object and the events.

To send an event to the caller, the MFT performs the following steps inside <b>ProcessOutput</b>:

<ol>
<li>
              Create a new collection object by calling <a href="https://msdn.microsoft.com/6a7bf7b6-62f1-4eac-9849-39021ee50f42">MFCreateCollection</a>.
            </li>
<li>
              Add one or more events to the collection by calling <a href="https://msdn.microsoft.com/1ef2463b-3d5e-4ed0-ab7c-68758e6cc056">IMFCollection::AddElement</a>.
            </li>
<li>
              Set the <b>pEvents</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure equal to the <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> pointer. The MFT leaves a reference count on this interface; the caller must release the pointer.
            </li>
</ol>
Events do not have time stamps. The caller should process the events before processing the output samples. In other words, events occur at the point in the stream immediately after the previous call to <b>ProcessOutput</b>, and prior to any output samples returned from the current <b>ProcessOutput</b> call.

It is valid for the <b>ProcessOutput</b> method to return one or more events and zero output samples.

The caller is responsible for releasing any events that the MFT allocates. When the method returns, check the <b>pEvents</b> member of each <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure. If the value is not <b>NULL</b>, the caller must release the <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> interface pointer:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Release the events that an MFT might allocate in IMFTransform::ProcessOutput().
void ReleaseEventCollection(DWORD cOutputBuffers, MFT_OUTPUT_DATA_BUFFER* pBuffers)
{
    for (DWORD i = 0; i &lt; cOutputBuffers; i++)
    {
        if (pBuffers[i].pEvents)
        {
            pBuffers[i].pEvents-&gt;Release();
            pBuffers[i].pEvents = NULL;
        }
    }
}
</pre>
</td>
</tr>
</table></span></div>
An MFT should not use the <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a> interface to send in-band events.

<h3><a id="Stream_Changes"></a><a id="stream_changes"></a><a id="STREAM_CHANGES"></a>Stream Changes</h3>
The <b>ProcessOutput</b> method can cause any of the following changes in an output stream:

<ul>
<li>
              The deletion of an output stream. To signal a stream deletion, the MFT sets the <b>MFT_OUTPUT_DATA_BUFFER_STREAM_END</b> flag in the <b>dwStatus</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure for that stream.
            </li>
<li>
              The creation of a new output stream. To signal a new output stream, the MFT sets the <b>MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS</b> flag in the <i>pdwStatus</i> parameter. A new stream can have the same stream identifier as a deleted stream.
            </li>
<li>
              A format change on an output stream. To signal a format change, the MFT sets the <b>MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE</b> flag in the <b>dwStatus</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure for that stream.
            </li>
</ul>
It is possible that all three of these actions will result from a single call to <b>ProcessOutput</b>. The caller must respond to them in the order listed here—first deletions, then additions, then format changes.

The <b>MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE</b> flag signals a format change on an output stream. This might mean the current media type has become invalid, or the preference order has changed and a more efficient format is available. In the latter case, it is possible that the client will re-set the original media type. To guard against endless loops, the MFT should not set the <b>MFT_OUTPUT_DATA_BUFFER_FORMAT_CHANGE</b> flag again until there is another change. Also, avoid setting this flag if the preference order changes but the current media type is still the most preferred type.

<h3><a id="Sample_Attributes"></a><a id="sample_attributes"></a><a id="SAMPLE_ATTRIBUTES"></a>Sample Attributes</h3>
An input sample might have attributes, which are accessed through the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. Unless a specific attribute no longer applies, all attributes should be copied into the corresponding output sample. The responsibily for copying attributes is determined as follows:

<ul>
<li>
              If the value of the <a href="https://msdn.microsoft.com/039ecb35-9aa9-4e8a-bbbc-042b9c4c874c">MFPKEY_EXATTRIBUTE_SUPPORTED</a> property on the MFT is <b>VARIANT_TRUE</b>, the MFT copies the attributes.
            </li>
<li>
              If the value of <a href="https://msdn.microsoft.com/039ecb35-9aa9-4e8a-bbbc-042b9c4c874c">MFPKEY_EXATTRIBUTE_SUPPORTED</a> is <b>VARIANT_FALSE</b>, or the property is not set, the client must copy the sample attributes. Do not overwrite any attributes that the MFT sets on the output sample.
            </li>
</ul>
For a list of sample attributes, see <a href="https://msdn.microsoft.com/64aead5a-61c4-4e83-a556-af33e0aa82be">Sample Attributes</a>.

<h3><a id="Asynchronous_Processing"></a><a id="asynchronous_processing"></a><a id="ASYNCHRONOUS_PROCESSING"></a>Asynchronous Processing</h3>
The previous remarks describe the <i>synchronous</i> processing model. To support asynchronous processing, see <a href="asynchronous_mfts.htm">Asynchronous MFTs</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

