---
UID: NF:mediaobj.IMediaObject.ProcessOutput
title: IMediaObject::ProcessOutput (mediaobj.h)
description: The ProcessOutput method generates output from the current input data.
helpviewer_keywords: ["IMediaObject interface [DirectShow]","ProcessOutput method","IMediaObject.ProcessOutput","IMediaObject::ProcessOutput","IMediaObjectProcessOutput","ProcessOutput","ProcessOutput method [DirectShow]","ProcessOutput method [DirectShow]","IMediaObject interface","dshow.imediaobject_processoutput","mediaobj/IMediaObject::ProcessOutput"]
old-location: dshow\imediaobject_processoutput.htm
tech.root: dshow
ms.assetid: 1a3b1192-f1e9-4f04-b543-d38692502b8e
ms.date: 4/26/2023
ms.keywords: IMediaObject interface [DirectShow],ProcessOutput method, IMediaObject.ProcessOutput, IMediaObject::ProcessOutput, IMediaObjectProcessOutput, ProcessOutput, ProcessOutput method [DirectShow], ProcessOutput method [DirectShow],IMediaObject interface, dshow.imediaobject_processoutput, mediaobj/IMediaObject::ProcessOutput
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::ProcessOutput
 - mediaobj/IMediaObject::ProcessOutput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.ProcessOutput
---

# IMediaObject::ProcessOutput


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ProcessOutput</code> method generates output from the current input data.

## -parameters

### -param dwFlags

Bitwise combination of zero or more flags from the <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_process_output_flags">DMO_PROCESS_OUTPUT_FLAGS</a> enumeration.

### -param cOutputBufferCount

Number of output buffers.

### -param pOutputBuffers [in, out]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer">DMO_OUTPUT_DATA_BUFFER</a> structures containing the output buffers. Specify the size of the array in the <i>cOutputBufferCount</i> parameter.

### -param pdwStatus [out]

Pointer to a variable that receives a reserved value (zero). The application should ignore this value.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No output was generated

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

The <i>pOutputBuffers</i> parameter points to an array of <b>DMO_OUTPUT_DATA_BUFFER</b> structures. The application must allocate one structure for each output stream. To determine the number of output streams, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getstreamcount">IMediaObject::GetStreamCount</a> method. Set the <i>cOutputBufferCount</i> parameter to this number.

Each <b>DMO_OUTPUT_DATA_BUFFER</b> structure contains a pointer to a buffer's <a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer</a> interface. The application allocates these buffers. The other members of the structure are status fields. The DMO sets these fields if the method succeeds. If the method fails, their values are undefined.

When the application calls <code>ProcessOutput</code>, the DMO processes as much input data as possible. It writes the output data to the output buffers, starting from the end of the data in each buffer. (To find the end of the data, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength">IMediaBuffer::GetBufferAndLength</a> method.) The DMO never holds a reference count on an output buffer.

If the DMO fills an entire output buffer and still has input data to process, the DMO returns the DMO_OUTPUT_DATA_BUFFERF_INCOMPLETE flag in the <b>DMO_OUTPUT_DATA_BUFFER</b> structure. The application should check for this flag by testing the <b>dwStatus</b> member of each structure.

If the method returns S_FALSE, no output was generated. However, a DMO is not required to return S_FALSE in this situation; it might return S_OK.

<b>Discarding data:</b>

You can discard data from a stream by setting the DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag in the <i>dwFlags</i> parameter. For each stream that you want to discard, set the <b>pBuffer</b> member of the <b>DMO_OUTPUT_DATA_BUFFER</b> structure to <b>NULL</b>.

For each stream in which <b>pBuffer</b> is <b>NULL</b>:

<ul>
<li>If the DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER flag is set, and the stream is discardable or optional, the DMO discards the data.</li>
<li>If the flag is set but the stream is neither discardable nor optional, the DMO discards the data if possible. It is not guaranteed to discard the data.</li>
<li>If the flag is not set, the DMO does not produce output data for that stream, but does not discard the data.</li>
</ul>
To check whether a stream is discardable or optional, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo">IMediaObject::GetOutputStreamInfo</a> method.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>