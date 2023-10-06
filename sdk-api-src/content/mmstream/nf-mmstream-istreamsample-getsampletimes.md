---
UID: NF:mmstream.IStreamSample.GetSampleTimes
title: IStreamSample::GetSampleTimes (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the current sample's start and end times. If the sample is updating, this method returns the times after the update completes.
helpviewer_keywords: ["GetSampleTimes","GetSampleTimes method [DirectShow]","GetSampleTimes method [DirectShow]","IStreamSample interface","IStreamSample interface [DirectShow]","GetSampleTimes method","IStreamSample.GetSampleTimes","IStreamSample::GetSampleTimes","IStreamSampleGetSampleTimes","dshow.istreamsample_getsampletimes","mmstream/IStreamSample::GetSampleTimes"]
old-location: dshow\istreamsample_getsampletimes.htm
tech.root: dshow
ms.assetid: d8c716fe-6731-4b54-9b4b-3b0f896f176b
ms.date: 4/26/2023
ms.keywords: GetSampleTimes, GetSampleTimes method [DirectShow], GetSampleTimes method [DirectShow],IStreamSample interface, IStreamSample interface [DirectShow],GetSampleTimes method, IStreamSample.GetSampleTimes, IStreamSample::GetSampleTimes, IStreamSampleGetSampleTimes, dshow.istreamsample_getsampletimes, mmstream/IStreamSample::GetSampleTimes
req.header: mmstream.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamSample::GetSampleTimes
 - mmstream/IStreamSample::GetSampleTimes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IStreamSample.GetSampleTimes
---

# IStreamSample::GetSampleTimes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

The <i>pCurrentTime</i> parameter enables you to conveniently track the media stream's current time, so you don't have to call <a href="/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-gettime">IMultiMediaStream::GetTime</a>. Unlike <b>GetTime</b>, however, this method returns S_OK if the stream doesn't have a clock; <b>GetTime</b> returns S_FALSE. The value assigned to <i>pCurrentTime</i> is the same as the value produced by the following code fragment.


```cpp

IMediaStream *pMediaStream = 0;
hr = pSample->GetMediaStream(&pMediaStream);
if (SUCCEEDED(hr))
{
  IMultiMediaStream *pMultiMediaStream = 0;
  hr = pMediaStream->GetMultiMediaStream(&pMultiMediaStream);
  pMediaStream->Release();
  if (SUCCEEDED(hr))
  {
    STREAM_TIME CurrentTime = 0;
    hr = pMultiMediaStream->GetTime(&CurrentTime);
    pMultiMediaStream->Release();
  }
}

```

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample Interface</a>



<a href="/windows/desktop/DirectShow/multimedia-streaming-data-types">Multimedia Streaming Data Types</a>