---
UID: NF:strmif.ICaptureGraphBuilder2.ControlStream
title: ICaptureGraphBuilder2::ControlStream (strmif.h)
description: The ControlStream method sets the start and stop times for one or more streams of captured data.
helpviewer_keywords: ["ControlStream","ControlStream method [DirectShow]","ControlStream method [DirectShow]","ICaptureGraphBuilder2 interface","ICaptureGraphBuilder2 interface [DirectShow]","ControlStream method","ICaptureGraphBuilder2.ControlStream","ICaptureGraphBuilder2::ControlStream","ICaptureGraphBuilder2ControlStream","dshow.icapturegraphbuilder2_controlstream","strmif/ICaptureGraphBuilder2::ControlStream"]
old-location: dshow\icapturegraphbuilder2_controlstream.htm
tech.root: dshow
ms.assetid: f5c91444-6ddb-403c-bff5-33d9ce91fae3
ms.date: 4/26/2023
ms.keywords: ControlStream, ControlStream method [DirectShow], ControlStream method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],ControlStream method, ICaptureGraphBuilder2.ControlStream, ICaptureGraphBuilder2::ControlStream, ICaptureGraphBuilder2ControlStream, dshow.icapturegraphbuilder2_controlstream, strmif/ICaptureGraphBuilder2::ControlStream
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICaptureGraphBuilder2::ControlStream
 - strmif/ICaptureGraphBuilder2::ControlStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICaptureGraphBuilder2.ControlStream
---

# ICaptureGraphBuilder2::ControlStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ControlStream</code> method sets the start and stop times for one or more streams of captured data.

## -parameters

### -param pCategory [in]

A pointer to a GUID that specifies one of the pin categories listed in <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>. The value of this parameter cannot be <b>NULL</b>.

### -param pType [in]

Pointer to a major type GUID that specifies the media type, or <b>NULL</b>. If this parameter is <b>NULL</b>, set the <i>pFilter</i> parameter to <b>NULL</b> as well. Otherwise, you might control the wrong pin and get unpredictable results.

### -param pFilter [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface that specifies which filter to control. To control all the capture filters in the graph, set this parameter to <b>NULL</b>.

### -param pstart [in]

Pointer to a variable that contains the start time. If the value is <b>MAXLONGLONG</b> (0x7FFFFFFFFFFFFFFF), the method cancels the previous start request. If the value is <b>NULL</b>, the pin starts immediately when the graph runs.

### -param pstop [in]

Pointer to a variable that contains the stop time. If the value is <b>MAXLONGLONG</b>, the method cancels any previous stop request. If the value is <b>NULL</b>, the pin stops immediately.

### -param wStartCookie [in]

Value that is sent as the second parameter of the <a href="/windows/desktop/DirectShow/ec-stream-control-started">EC_STREAM_CONTROL_STARTED</a> event notification. See Remarks for more information.

### -param wStopCookie [in]

Value that is sent as the second parameter of the <a href="/windows/desktop/DirectShow/ec-stream-control-stopped">EC_STREAM_CONTROL_STOPPED</a> event notification. See Remarks for more information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
At least one downstream renderer will not send a stop notification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Could not find a matching pin, or the pin did not support stream control.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

This method locates output pins on capture filters, using search criteria that you supply in the method call. Then it calls the <a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl</a> methods on those pins. This method enables an application to control streams without the application needing to enumerate the filters and pins in the graph.

Use this method for frame-accurate capture, or for individual control of capture and preview. For example, you can stop capturing to disk but leave video preview running.

The first three parameters specify which pins to control. A capture graph can have more than one capture filter. For example, it might have filters for video, audio, and closed captioning data. Also, a capture filter can have more than one output pin. Some capture filters have separate pins for preview and capture, or separate pins for video-only data and audio-video interleaved data. To control video preview, for example, specify PIN_CATEGORY_PREVIEW for <i>pCategory</i> and MEDIATYPE_Video for <i>pType</i>.

<div class="alert"><b>Note</b>  <p class="note">If the pin category is PIN_CATEGORY_PREVIEW, you cannot set specific start and stop times, because the samples delivered by a preview pin have no time stamps (see <a href="/windows/desktop/DirectShow/time-stamps">Time Stamps</a>). Instead, use the values <b>NULL</b> and <b>MAXLONGLONG</b> to start and stop the pin at the desired times.

<p class="note">Also, this method is not supported for preview if the device uses a video port pin, because in that case the device is delivering the preview samples directly over hardware.

</div>
<div> </div>
To control a pin, this method calls the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-startat">IAMStreamControl::StartAt</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-stopat">IAMStreamControl::StopAt</a> methods. Each pin sends an <a href="/windows/desktop/DirectShow/ec-stream-control-started">EC_STREAM_CONTROL_STARTED</a> event notification when it starts. The second parameter of the event notification is the value given in <i>wStartCookie</i>. When the pin stops, it sends an <a href="/windows/desktop/DirectShow/ec-stream-control-stopped">EC_STREAM_CONTROL_STOPPED</a> event notification. The second parameter of that event notification is the value given in <i>wStopCookie</i>.

When this method locates a matching pin, it searches downstream for another filter that supports <a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl</a> (typically a multiplexer). If it finds one, it also sets the start and stop times on that filter. This generates two pairs of stop notifications: one for the capture filter, and one for the downstream filter. Only the stop notification from the downstream filter uses the <i>wStopCookie</i> parameter. Waiting for this event guarantees that the downstream filter receives the last sample.

If no downstream filter supports <b>IAMStreamControl</b>, the method returns S_FALSE. In that case, you might receive the stop notification before the last sample is rendered.

<b>MAXLONGLONG</b> is the largest possible <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> value. In the DirectShow base class library, it is also defined as the constant <b>MAX_TIME</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>