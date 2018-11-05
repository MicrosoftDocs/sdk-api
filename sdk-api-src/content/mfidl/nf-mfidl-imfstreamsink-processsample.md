---
UID: NF:mfidl.IMFStreamSink.ProcessSample
title: IMFStreamSink::ProcessSample
author: windows-sdk-content
description: Delivers a sample to the stream. The media sink processes the sample.
old-location: mf\imfstreamsink_processsample.htm
tech.root: medfound
ms.assetid: 30e2bdb5-a99d-4a2e-ab36-7b4e383c645f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 30e2bdb5-a99d-4a2e-ab36-7b4e383c645f, IMFStreamSink interface [Media Foundation],ProcessSample method, IMFStreamSink.ProcessSample, IMFStreamSink::ProcessSample, ProcessSample, ProcessSample method [Media Foundation], ProcessSample method [Media Foundation],IMFStreamSink interface, mf.imfstreamsink_processsample, mfidl/IMFStreamSink::ProcessSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
 - IMFStreamSink.ProcessSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFStreamSink::ProcessSample


## -description



Delivers a sample to the stream. The media sink processes the sample.




## -parameters




### -param pSample [in]

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of a sample that contains valid data for the stream.


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
<dt><b>MF_E_INVALID_STATE_TRANSITION</b></dt>
</dl>
</td>
<td width="60%">
The media sink is in the wrong state to receive a sample. For example, preroll is complete but the presenation clock has not started yet.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALID_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
The sample has an invalid time stamp. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The media sink is paused or stopped and cannot process the sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_CLOCK</b></dt>
</dl>
</td>
<td width="60%">
The presentation clock was not set. Call <a href="https://msdn.microsoft.com/844fc3b3-b56e-4048-b589-e24457bcc419">IMFMediaSink::SetPresentationClock</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_SAMPLE_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
The sample does not have a time stamp.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The stream sink has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">Shutdown</a> method has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.

</td>
</tr>
</table>
 




## -remarks



Call this method when the stream sink sends an <a href="https://msdn.microsoft.com/35020a15-942f-4dd0-9ca4-815affdacecf">MEStreamSinkRequestSample</a> event.

This method can return MF_E_INVALID_TIMESTAMP for various reasons, depending on the implementation of the media sink:

<ul>
<li>
Negative time stamps.

</li>
<li>
Time stamps that jump backward (within the same stream).

</li>
<li>
The time stamps for one stream have drifted too far from the time stamps on another stream within the same media sink (for example, an archive sink that multiplexes the streams).

</li>
</ul>
Not every media sink returns an error code in these situations.




## -see-also




<a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

