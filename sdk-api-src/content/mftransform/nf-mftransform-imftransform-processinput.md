---
UID: NF:mftransform.IMFTransform.ProcessInput
title: IMFTransform::ProcessInput
author: windows-sdk-content
description: Delivers data to an input stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_processinput.htm
tech.root: medfound
ms.assetid: c94d406b-7cd9-42d4-ae9e-3d21dbb47209
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IMFTransform interface [Media Foundation],ProcessInput method, IMFTransform.ProcessInput, IMFTransform::ProcessInput, ProcessInput, ProcessInput method [Media Foundation], ProcessInput method [Media Foundation],IMFTransform interface, c94d406b-7cd9-42d4-ae9e-3d21dbb47209, mf.imftransform_processinput, mftransform/IMFTransform::ProcessInput
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.ProcessInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTransform::ProcessInput


## -description


Delivers data to an input stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pSample [in]

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the input sample. The sample must contain at least one media buffer that contains valid input data.
          


### -param dwFlags [in]

Reserved. Must be zero.
          


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_SAMPLE_DURATION</b></dt>
</dl>
</td>
<td width="60%">
The input sample requires a valid sample duration. To set the duration, call <a href="https://msdn.microsoft.com/f97be98e-8f1b-4bae-8cdd-8bdfe107894d">IMFSample::SetSampleDuration</a>. 

Some MFTs require that input samples have valid durations. Some MFTs do not require sample durations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_SAMPLE_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
The input sample requires a time stamp. To set the time stamp, call <a href="https://msdn.microsoft.com/59d32002-2f5c-4a94-bd09-fd5a2c005ffc">IMFSample::SetSampleTime</a>. 

Some MFTs require that input samples have valid time stamps. Some MFTs do not require time stamps.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The transform cannot process more input at this time.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type is not set on one or more streams.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_D3D_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The media type is not supported for DirectX Video Acceleration (DXVA). A DXVA-enabled decoder might return this error code.
              

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you are converting a DirectX Media Object (DMO) to an MFT, be aware that <b>S_FALSE</b> is not a valid return code for <b>IMFTransform::ProcessInput</b>, unlike the <b>IMediaObject::ProcessInput</b> method.</div>
<div> </div>



## -remarks



In most cases, if the method succeeds, the MFT stores the sample and holds a reference count on the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> pointer. Do not re-use the sample until the MFT releases the sample. Instead of storing the sample, however, an MFT might copy the sample data into a new buffer. In that case, the MFT should set the <b>MFT_INPUT_STREAM_DOES_NOT_ADDREF</b> flag in the <a href="https://msdn.microsoft.com/d57ffac7-1a92-4c6b-bd59-0acd7239c0a6">IMFTransform::GetInputStreamInfo</a> method.
      

If the MFT already has enough input data to produce an output sample, it does not accept new input data, and <b>ProcessInput</b> returns <b>MF_E_NOTACCEPTING</b>. At that point, the client should clear the pending input data by doing one of the following:
        

<ul>
<li>Generate new output by calling <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>.
          </li>
<li>Flush the input data by calling <a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">IMFTransform::ProcessMessage</a> with the MFT_<b>MESSAGE_COMMAND_FLUSH</b> message.
          </li>
</ul>
An exception to this rule is the <b>MFT_OUTPUT_STREAM_LAZY_READ</b> flag. When this flag is present, the transform will discard stored samples if you give it more input. For more information, see <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a>. A transform should never queue any more input data than is required to produce the correct output.
      

An MFT can process the input data in the <b>ProcessInput</b> method. However, most MFTs wait until the client calls <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>.
      

After the client has set valid media types on all of the streams, the MFT should always be in one of two states: Able to accept more input, or able to produce more output. It should never be in both states or neither state. An MFT should only accept as much input as it needs to generate at least one output sample, at which point <b>ProcessInput</b> returns <b>MF_E_NOTACCEPTING</b>. When <b>ProcessInput</b> returns <b>MF_E_NOTACCEPTING</b>, the client can assume that the MFT is ready to produce output.
      

If an MFT encounters a non-fatal error in the input data, it can simply drop the data and attempt to recover when it gets the more input data. To request more input data, the MFT returns <b>MF_E_TRANSFORM_NEED_MORE_INPUT</b> from the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> method. If the MFT drops any data, it should set the <a href="https://msdn.microsoft.com/f9e1e700-9958-404d-8b83-08f846f5a1b0">MFSampleExtension_Discontinuity</a> attribute attribute on the next output sample, to notify the caller that there is a gap in the data stream.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTProcessInput</b>. See <a href="https://msdn.microsoft.com/en-us/library/Bb250374(v=VS.85).aspx">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Asynchronous_Processing"></a><a id="asynchronous_processing"></a><a id="ASYNCHRONOUS_PROCESSING"></a>Asynchronous Processing</h3>
The previous remarks describe the <i>synchronous</i> processing model. To support asynchronous processing, see <a href="https://msdn.microsoft.com/en-us/library/Dd317909(v=VS.85).aspx">Asynchronous MFTs</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

