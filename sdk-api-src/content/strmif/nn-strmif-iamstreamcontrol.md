---
UID: NN:strmif.IAMStreamControl
title: IAMStreamControl (strmif.h)
description: The IAMStreamControl interface controls individual streams on a filter.
helpviewer_keywords: ["IAMStreamControl","IAMStreamControl interface [DirectShow]","IAMStreamControl interface [DirectShow]","described","IAMStreamControlInterface","dshow.iamstreamcontrol","strmif/IAMStreamControl"]
old-location: dshow\iamstreamcontrol.htm
tech.root: dshow
ms.assetid: 126c7ed7-acc0-4248-a3ab-c91c9f1c5cee
ms.date: 4/26/2023
ms.keywords: IAMStreamControl, IAMStreamControl interface [DirectShow], IAMStreamControl interface [DirectShow],described, IAMStreamControlInterface, dshow.iamstreamcontrol, strmif/IAMStreamControl
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
 - IAMStreamControl
 - strmif/IAMStreamControl
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
 - IAMStreamControl
---

# IAMStreamControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMStreamControl</code> interface controls individual streams on a filter. Pins on some filters expose this interface. For example, the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux Filter</a> supports this interface on its input pins, and the <a href="/windows/desktop/DirectShow/audio-capture-filter">Audio Capture Filter</a> and <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> support it on their output pins.

This interface enables an application to turn streams on and off at specified times. For example, an application might turn off an audio stream to mute the audio during video preview. Capture applications can use this interface to specify exact start and stop times for capture, and to control capture and preview streams independently of each other.

To use this interface, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-startat">IAMStreamControl::StartAt</a> method to specify when the pin will start delivering data, and the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-stopat">IAMStreamControl::StopAt</a> method to specify when it will stop delivering data. Then call <a href="/windows/desktop/api/control/nf-control-imediacontrol-run">IMediaControl::Run</a> on the Filter Graph Manager to run the filter graph. All times are relative to when the graph starts running.

When you use this interface, be aware of the following limitations:

<ul>
<li>There must be a reference clock in the filter graph.</li>
<li>Preview pins on capture cards with hardware overlay do not support this interface.</li>
<li>If you are capturing audio and video to an interleaved AVI file, the AVI Mux filter requires data both streams. If you stop one stream, the filter cannot interleave the data. For more information, see <a href="/windows/desktop/api/strmif/nn-strmif-iconfiginterleaving">IConfigInterleaving Interface</a>.</li>
</ul>
Depending on the application, you might find the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-controlstream">ICaptureGraphBuilder2::ControlStream</a> method more convenient, because it supports stream control at the graph level, so that you do not have to enumerate individual filters and pins.

<b>Filter developers</b>: The <a href="/windows/desktop/DirectShow/cbasestreamcontrol">CBaseStreamControl</a> base class implements this interface.

## -inheritance

The <b>IAMStreamControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMStreamControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/cbasestreamcontrol">CBaseStreamControl Class</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>
