---
UID: NF:strmif.ICaptureGraphBuilder.RenderStream
title: ICaptureGraphBuilder::RenderStream (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Connects a source filter's pin, of an optionally specified category, to the rendering filter, and optionally through another filter.
helpviewer_keywords: ["ICaptureGraphBuilder interface [DirectShow]","RenderStream method","ICaptureGraphBuilder.RenderStream","ICaptureGraphBuilder::RenderStream","ICaptureGraphBuilderRenderStream","RenderStream","RenderStream method [DirectShow]","RenderStream method [DirectShow]","ICaptureGraphBuilder interface","dshow.icapturegraphbuilder_renderstream","strmif/ICaptureGraphBuilder::RenderStream"]
old-location: dshow\icapturegraphbuilder_renderstream.htm
tech.root: dshow
ms.assetid: 2b174f31-d7bb-4934-9d5b-2e4fd6ae8bf5
ms.date: 4/26/2023
ms.keywords: ICaptureGraphBuilder interface [DirectShow],RenderStream method, ICaptureGraphBuilder.RenderStream, ICaptureGraphBuilder::RenderStream, ICaptureGraphBuilderRenderStream, RenderStream, RenderStream method [DirectShow], RenderStream method [DirectShow],ICaptureGraphBuilder interface, dshow.icapturegraphbuilder_renderstream, strmif/ICaptureGraphBuilder::RenderStream
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
 - ICaptureGraphBuilder::RenderStream
 - strmif/ICaptureGraphBuilder::RenderStream
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
 - ICaptureGraphBuilder.RenderStream
---

# ICaptureGraphBuilder::RenderStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Connects a source filter's pin, of an optionally specified category, to the rendering filter, and optionally through another filter.

## -parameters

### -param pCategory [in]

Pointer to a GUID specifying which output pin of the source filter to connect. See <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a> for a list of all pin categories. <b>NULL</b> indicates render the only output pin, regardless of category.

### -param pSource [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> or an <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface representing either the source filter or an output pin. Source filters are typically a file source filter, such as an AVI file source filter or a capture filter.

### -param pfCompressor [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface representing the optional compression filter.

### -param pfRenderer [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface representing the renderer. You can use the <i>ppf</i> (multiplexer) parameter from <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-setoutputfilename">ICaptureGraphBuilder::SetOutputFileName</a> to supply this value.

## -returns

Returns VFW_S_NOPREVIEWPIN if the capture filter has a capture pin but no preview pin, and you call <code>RenderStream</code> with the &amp;PIN_CATEGORY_PREVIEW category on the capture pin. In this case, <code>RenderStream</code> will render the preview pin of the <a href="/windows/desktop/DirectShow/smart-tee-filter">Smart Tee</a> filter. For more information, see Remarks.

## -remarks

If you specify a non-<b>NULL</b><a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a> GUID for <i>pCategory</i> and a capture filter for <i>pSource</i>, this method instantiates and connects additional required upstream filters, such as TV tuners and crossbars. It then renders the capture pin of <i>pSource</i>.

If <i>pSource</i> is a pin, then specify <b>NULL</b> for <i>pCategory</i> and this method renders the stream from that pin.

If the source filter has only one output pin, specify <b>NULL</b> for <i>pCategory</i>.

<i>pSource</i>, <i>pfCompressor</i>, and <i>pfRenderer</i> filters given as parameters must be present in the graph before this method is called.

If you are building a capture graph that is using WDM capture filters, this method will build all necessary upstream filters as well as the downstream filters.

Some capture filters that work with new WDM VPE (Video Port Extension) video capture hardware have video port pins instead of preview pins meant for previewing. Video port pins do not connect directly to a video renderer, but instead to a special filter called the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>. Your application does not need to worry about this. All you have to do is call <code>RenderStream</code> with PIN_CATEGORY_PREVIEW and the capture graph builder will correctly render the VIDEO PORT pin through an overlay mixer if that is what is necessary.

When you render a capture or preview pin of a video capture filter (using <code>RenderStream</code> with the PIN_CATEGORY_CAPTURE or PIN_CATEGORY_PREVIEW category) and the capture filter has a capture pin but no preview pin, the <a href="/windows/desktop/DirectShow/smart-tee-filter">Smart Tee</a> filter will be used automatically to allow simultaneous capture and preview. For example, calling <code>RenderStream</code> with the PIN_CATEGORY_CAPTURE category will actually connect a Smart Tee filter to the capture pin of the filter, and then render the capture pin of the Smart Tee. If you then call <code>RenderStream</code> with the PIN_CATEGORY_PREVIEW category on the capture pin, it will actually render the preview pin of the Smart Tee. If calling <code>RenderStream</code> with PIN_CATEGORY_PREVIEW results in using the capture pin and a Smart Tee filter, <code>RenderStream</code> will return VFW_S_NOPREVIEWPIN to indicate this. Thus, if <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-findinterface">FindInterface</a> fails to find a preview interface, you may need to call <b>FindInterface</b> with the PIN_CATEGORY_PREVIEW category and with the PIN_CATEGORY_CAPTURE category, because the preview interface can be found by looking downstream of the capture pin of the capture filter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>