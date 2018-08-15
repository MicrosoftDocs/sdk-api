---
UID: NF:mmstream.IStreamSample.GetSampleTimes
title: IStreamSample::GetSampleTimes
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves the current sample's start and end times. If the sample is updating, this method returns the times after the update completes.
old-location: dshow\istreamsample_getsampletimes.htm
old-project: DirectShow
ms.assetid: d8c716fe-6731-4b54-9b4b-3b0f896f176b
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetSampleTimes, GetSampleTimes method [DirectShow], GetSampleTimes method [DirectShow],IStreamSample interface, IStreamSample interface [DirectShow],GetSampleTimes method, IStreamSample.GetSampleTimes, IStreamSample::GetSampleTimes, IStreamSampleGetSampleTimes, dshow.istreamsample_getsampletimes, mmstream/IStreamSample::GetSampleTimes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmstream.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: STREAM_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IStreamSample.GetSampleTimes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStreamSample::GetSampleTimes


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the current sample's start and end times. If the sample is updating, this method returns the times after the update completes.




## -parameters




### -param pStartTime [out]

Pointer to a STREAM_TIME value that will contain the sample's start time.


### -param pEndTime [out]

Pointer to a STREAM_TIME value that will contain the sample's end time.


### -param pCurrentTime [out]

Pointer to a STREAM_TIMEvalue that will contain the media stream's current media time.


## -returns



Returns S_OK if successful or E_POINTER if one of the parameters is invalid.




## -remarks



For streams that have a clock, the start and end times will be relative to the stream's current time. If the stream doesn't have a clock, the times are media-relative and the current time will be zero.

The <i>pCurrentTime</i> parameter enables you to conveniently track the media stream's current time, so you don't have to call <a href="https://msdn.microsoft.com/da92c68b-176c-4773-9ae1-63f803bc206e">IMultiMediaStream::GetTime</a>. Unlike <b>GetTime</b>, however, this method returns S_OK if the stream doesn't have a clock; <b>GetTime</b> returns S_FALSE. The value assigned to <i>pCurrentTime</i> is the same as the value produced by the following code fragment.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IMediaStream *pMediaStream = 0;
hr = pSample-&gt;GetMediaStream(&amp;pMediaStream);
if (SUCCEEDED(hr))
{
  IMultiMediaStream *pMultiMediaStream = 0;
  hr = pMediaStream-&gt;GetMultiMediaStream(&amp;pMultiMediaStream);
  pMediaStream-&gt;Release();
  if (SUCCEEDED(hr))
  {
    STREAM_TIME CurrentTime = 0;
    hr = pMultiMediaStream-&gt;GetTime(&amp;CurrentTime);
    pMultiMediaStream-&gt;Release();
  }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample Interface</a>



<a href="https://msdn.microsoft.com/750a7992-e2ef-4149-b1c8-c5201f6af035">Multimedia Streaming Data Types</a>
 

 

