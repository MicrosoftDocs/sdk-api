---
UID: NF:mfidl.IMFMediaSource.Start
title: IMFMediaSource::Start (mfidl.h)
description: Starts, seeks, or restarts the media source by specifying where to start playback.
helpviewer_keywords: ["0a5abafe-1525-4bda-946c-05a6145e57ee","IMFMediaSource interface [Media Foundation]","Start method","IMFMediaSource.Start","IMFMediaSource::Start","Start","Start method [Media Foundation]","Start method [Media Foundation]","IMFMediaSource interface","mf.imfmediasource_start","mfidl/IMFMediaSource::Start"]
old-location: mf\imfmediasource_start.htm
tech.root: mf
ms.assetid: 0a5abafe-1525-4bda-946c-05a6145e57ee
ms.date: 12/05/2018
ms.keywords: 0a5abafe-1525-4bda-946c-05a6145e57ee, IMFMediaSource interface [Media Foundation],Start method, IMFMediaSource.Start, IMFMediaSource::Start, Start, Start method [Media Foundation], Start method [Media Foundation],IMFMediaSource interface, mf.imfmediasource_start, mfidl/IMFMediaSource::Start
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSource::Start
 - mfidl/IMFMediaSource::Start
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSource.Start
---

# IMFMediaSource::Start


## -description

Starts, seeks, or restarts the media source by specifying where to start playback.

## -parameters

### -param pPresentationDescriptor [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the media source's presentation descriptor. To get the presentation descriptor, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">IMFMediaSource::CreatePresentationDescriptor</a>. You can modify the presentation descriptor before calling <b>Start</b>, to select or deselect streams or change the media types.

### -param pguidTimeFormat [in]

Pointer to a GUID that specifies the time format. The time format defines the units for the <i>pvarStartPosition</i> parameter. If the value <i></i> is <b>GUID_NULL</b>, the time format is 100-nanosecond units. Some media sources might support additional time format GUIDs. This parameter can be <b>NULL</b>. If the value is <b>NULL</b>, it is equivalent to <b>GUID_NULL</b>.

### -param pvarStartPosition [in]

Specifies where to start playback. The units of this parameter are indicated by the time format given in <i>pguidTimeFormat</i>. If the time format is <b>GUID_NULL</b>, the variant type must be <b>VT_I8</b> or <b>VT_EMPTY</b>. Use <b>VT_I8</b> to specify a new starting position, in 100-nanosecond units. Use <b>VT_EMPTY</b> to start from the current position. Other time formats might use other <b>PROPVARIANT</b> types.

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
<dt><b>MF_E_ASF_OUTOFRANGE</b></dt>
</dl>
</td>
<td width="60%">
The start position is past the end of the presentation (ASF media source).
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_HW_MFT_FAILED_START_STREAMING</b></dt>
</dl>
</td>
<td width="60%">
A hardware device was unable to start streaming. This error code can be returned by a media source that represents a hardware device, such as a camera. For example, if the camera is already being used by another application, the method might return this error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The start request is not valid. For example, the start position is past the end of the presentation.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_TIME_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The media source does not support the time format specified in <i>pguidTimeFormat</i>.
              

</td>
</tr>
</table>

## -remarks

This method is asynchronous. If the operation succeeds, the media source sends the following events:

<ul>
<li>For each new stream, the source sends an <a href="/windows/desktop/medfound/menewstream">MENewStream</a> event. This event is sent for the first <b>Start</b> call in which the stream appears. The event data is a pointer to the stream's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream">IMFMediaStream</a> interface.
          </li>
<li>For each <i>updated</i> stream, the source sends an <a href="/windows/desktop/medfound/meupdatedstream">MEUpdatedStream</a> event. A stream is updated if the stream already existed when <b>Start</b> was called (for example, if the application seeks during playback). The event data is a pointer to the stream's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream">IMFMediaStream</a> interface.
          </li>
<li>If the previous state was stopped, the source sends an <a href="/windows/desktop/medfound/mesourcestarted">MESourceStarted</a> event.
          </li>
<li>If the previous state was started or paused and the starting position is the current position (<b>VT_EMPTY</b>), the source sends an <a href="/windows/desktop/medfound/mesourcestarted">MESourceStarted</a> event.
          </li>
<li>If the previous state was started or paused, and a new starting position is specified, the source sends an <a href="/windows/desktop/medfound/mesourceseeked">MESourceSeeked</a> event.
          </li>
<li>If the source sends an <a href="/windows/desktop/medfound/mesourcestarted">MESourceStarted</a> event, each media stream sends an <a href="/windows/desktop/medfound/mestreamstarted">MEStreamStarted</a> event. If the source sends an <a href="/windows/desktop/medfound/mesourceseeked">MESourceSeeked</a> event, each stream sends an <a href="/windows/desktop/medfound/mestreamseeked">MEStreamSeeked</a> event.
          </li>
</ul>
If the start operation fails asynchronously (after the method returns <b>S_OK</b>), the media source sends an <a href="/windows/desktop/medfound/mesourcestarted">MESourceStarted</a> event that contains a failure code, without sending any of the other events listed here. If the method fails synchronously (returns an error code), no events are raised.
      

A call to <b>Start</b> results in a <i>seek</i> if the previous state was started or paused, and the new starting position is not <b>VT_EMPTY</b>. Not every media source can seek. If a media source can seek, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics">IMFMediaSource::GetCharacteristics</a> method returns the <b>MFMEDIASOURCE_CAN_SEEK</b> flag.
      

Events from the media source are not synchronized with events from the media streams. If you seek a media source, therefore, you can still receive samples from the earlier position after getting the <a href="/windows/desktop/medfound/mesourceseeked">MESourceSeeked</a> event. If you need to synchronize the operations, wait for the stream event, <a href="/windows/desktop/medfound/mestreamseeked">MEStreamSeeked</a>, which marks the exact point in the stream where the seek occurs.
      

<h3><a id="End_of_Stream"></a><a id="end_of_stream"></a><a id="END_OF_STREAM"></a>End of Stream</h3>
When a stream plays to the end, the stream sends an <a href="/windows/desktop/medfound/meendofstream">MEEndOfStream</a> event. When all of the selected streams have reached the end, the media source sends an <a href="/windows/desktop/medfound/meendofpresentation">MEEndOfPresentation</a> event.

If the starting position is past the end of a selected stream (but before the end of the presentation), the stream should send <a href="/windows/desktop/medfound/meendofstream">MEEndOfStream</a> immediately after <a href="/windows/desktop/medfound/mestreamstarted">MEStreamStarted</a>/<a href="/windows/desktop/medfound/mestreamseeked">MEStreamSeeked</a>. If playback reaches the end of the presentation and <b>Start</b> is called again from the current position, the streams re-send the MEEndOfStream event and the media source re-sends the <a href="/windows/desktop/medfound/meendofpresentation">MEEndOfPresentation</a> event. These events inform the pipeline not to request any more data.

During reverse playback, the start of the file is considered the end of the stream. For more information, see <a href="/windows/desktop/medfound/implementing-rate-control">Implementing Rate Control</a>.

<h3><a id="Implementing_Start"></a><a id="implementing_start"></a><a id="IMPLEMENTING_START"></a>Implementing Start</h3>
When a media source executes a seek, it should start at the first key frame before the seek time, so that the decoder can decode the samples for the target start time. The pipeline will discard any decoded samples that are too early.

If the start time is <b>VT_EMPTY</b> and the previous state was started or paused, the source should resume from its current position. In this case, it is not necessary to resend the previous key frame, because the decoder will still have the data that was previously sent.

When validating the  <i>pPresentationDescriptor</i> parameter, the media source should check only for the information that it needs to function correctly. In particular, the client can add private attributes to the presentation descriptor. The presence of additional attributes should not cause the <b>Start</b> method to fail.

After <b>Start</b> is called, each stream on the media source must do one of the following:

<ul>
<li>Deliver media data in response to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample">IMFMediaStream::RequestSample</a> calls.</li>
<li>Send <a href="/windows/desktop/medfound/mestreamtick">MEStreamTick</a> events to indicate a gap in the stream.</li>
<li>Send an <a href="/windows/desktop/medfound/meendofstream">MEEndOfStream</a> event to indicate the end of the stream.</li>
</ul>
For more information, see <a href="/windows/desktop/medfound/writing-a-custom-media-source">Writing a Custom Media Source</a>.


#### Examples

The following example starts playback at 1 second into the presentation.
        


```
PROPVARIANT var;
PropVariantInit(&var);
var.vt = VT_I8;
var.hVal.QuadPart = 10000000; // 10^7 = 1 second.

hr = pSource->Start(pPresentationDescriptor, NULL, &var);

```

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>