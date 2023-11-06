---
UID: NF:strmif.ICaptureGraphBuilder.ControlStream
title: ICaptureGraphBuilder::ControlStream (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Sends stream control messages to the pin of the specified category on one or more capture filters in a graph.
helpviewer_keywords: ["ControlStream","ControlStream method [DirectShow]","ControlStream method [DirectShow]","ICaptureGraphBuilder interface","ICaptureGraphBuilder interface [DirectShow]","ControlStream method","ICaptureGraphBuilder.ControlStream","ICaptureGraphBuilder::ControlStream","ICaptureGraphBuilderControlStream","dshow.icapturegraphbuilder_controlstream","strmif/ICaptureGraphBuilder::ControlStream"]
old-location: dshow\icapturegraphbuilder_controlstream.htm
tech.root: dshow
ms.assetid: 8d7d3a4d-3071-4829-99df-f0bcc9197b38
ms.date: 4/26/2023
ms.keywords: ControlStream, ControlStream method [DirectShow], ControlStream method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],ControlStream method, ICaptureGraphBuilder.ControlStream, ICaptureGraphBuilder::ControlStream, ICaptureGraphBuilderControlStream, dshow.icapturegraphbuilder_controlstream, strmif/ICaptureGraphBuilder::ControlStream
req.header: strmif.h
req.include-header: Dshow.h
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
 - ICaptureGraphBuilder::ControlStream
 - strmif/ICaptureGraphBuilder::ControlStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.ControlStream
---

# ICaptureGraphBuilder::ControlStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Sends stream control messages to the pin of the specified category on one or more capture filters in a graph.

## -parameters

### -param pCategory [in]

Pointer to a <b>GUID</b> specifying the output pin category. See <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a> for a list of all pin categories. This value cannot be <b>NULL</b>.

### -param pFilter [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface on the filter to control. Specifying <b>NULL</b> controls all capture filters in the graph. You will get one notification for each capture filter.

### -param pstart [in]

Pointer to the start time for capture. <b>NULL</b> means start now. <b>MAX_TIME</b> means cancel previous request, or take no action if there is no previous request.

### -param pstop [in]

Pointer to the stop time for capture. <b>NULL</b> means stop now. <b>MAX_TIME</b> means cancel previous request, or take no action if there is no previous request.

### -param wStartCookie [in]

Specifies a particular value to be sent when the start occurs.

### -param wStopCookie [in]

Specifies a particular value to be sent when the stop occurs.

## -returns

Returns S_FALSE if the stop notification is sent before the last sample sent by the capture filter is rendered, otherwise returns S_OK.

If this method returns S_FALSE, the application might want to wait before stopping the filter graph to allow all samples to pass through the graph and be rendered. Otherwise, samples might be lost. 



If there are no pins matching the description you provide, or if stream control cannot be supported on all of the indicated pins, this function will return a failure code.

## -remarks

Use this method for frame-accurate capture, or for individual control of capture and preview. For example, you could turn off writing of the captured image to disk if you only want to preview the captured image.

This method uses the <a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl</a> interface on the pins.

This method sends one notification for each filter found with a pin of the specified category.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>