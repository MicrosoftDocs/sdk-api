---
UID: NF:strmif.ICaptureGraphBuilder2.RenderStream
title: ICaptureGraphBuilder2::RenderStream (strmif.h)
description: The RenderStream method connects an output pin on a source filter to a sink filter, optionally through an intermediate filter.
helpviewer_keywords: ["ICaptureGraphBuilder2 interface [DirectShow]","RenderStream method","ICaptureGraphBuilder2.RenderStream","ICaptureGraphBuilder2::RenderStream","ICaptureGraphBuilder2RenderStream","RenderStream","RenderStream method [DirectShow]","RenderStream method [DirectShow]","ICaptureGraphBuilder2 interface","dshow.icapturegraphbuilder2_renderstream","strmif/ICaptureGraphBuilder2::RenderStream"]
old-location: dshow\icapturegraphbuilder2_renderstream.htm
tech.root: dshow
ms.assetid: 2fb5f13c-2bf5-463b-a209-77129a159bd6
ms.date: 4/26/2023
ms.keywords: ICaptureGraphBuilder2 interface [DirectShow],RenderStream method, ICaptureGraphBuilder2.RenderStream, ICaptureGraphBuilder2::RenderStream, ICaptureGraphBuilder2RenderStream, RenderStream, RenderStream method [DirectShow], RenderStream method [DirectShow],ICaptureGraphBuilder2 interface, dshow.icapturegraphbuilder2_renderstream, strmif/ICaptureGraphBuilder2::RenderStream
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICaptureGraphBuilder2::RenderStream
 - strmif/ICaptureGraphBuilder2::RenderStream
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
 - ICaptureGraphBuilder2.RenderStream
---

# ICaptureGraphBuilder2::RenderStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RenderStream</code> method connects an output pin on a source filter to a sink filter, optionally through an intermediate filter.

## -parameters

### -param pCategory [in]

A pointer to a GUID that specifies one of the pin categories listed in <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>. To match any pin, regardless of category, set this parameter to <b>NULL</b>. Typical values include the following.

<ul>
<li>PIN_CATEGORY_CAPTURE</li>
<li>PIN_CATEGORY_PREVIEW</li>
<li>PIN_CATEGORY_CC</li>
</ul>

### -param pType [in]

Pointer to a major-type GUID that specifies the media type of the output pin; or <b>NULL</b> to use any pin, regardless of media type. For a list of possible values, see <a href="/windows/desktop/DirectShow/major-types">Major Types</a>.

### -param pSource [in]

Specifies a pointer to the starting filter for the connection, or to an output pin.

### -param pfCompressor [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of an intermediate filter, such as a compression filter. Can be <b>NULL</b>.

### -param pfRenderer [in]

Pointer to the <b>IBaseFilter</b> interface of a sink filter, such as a renderer or mux filter. If the value is <b>NULL</b>, the method uses a default renderer (see Remarks).

## -returns

Returns an <b>HRESULT</b> value. Possible return values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_NOPREVIEWPIN</b></dt>
</dl>
</td>
<td width="60%">
Preview was rendered through the <a href="/windows/desktop/DirectShow/smart-tee-filter">Smart Tee Filter</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
A filter is not in the filter graph. This error can occur if you did not call <b>AddFilter</b> to add <i>pSource</i>, <i>pIntermediate</i>, or <i>pSink</i> to the graph. It can also occur if you did not call <b>SetFiltergraph</b> to connect your graph to the Capture Graph Builder; in this case, the Capture Graph Builder object automatically creates its own filter graph. See <a href="/windows/desktop/DirectShow/about-the-capture-graph-builder">About the Capture Graph Builder</a>.

</td>
</tr>
</table>

## -remarks

This method renders a stream by connecting two or more filters together in a chain:

<ul>
<li>The <i>pSource</i> parameter specifies the start of the chain, either a filter or an output pin.</li>
<li>The <i>pIntermediate</i> parameter specifies an intermediate filter, typically a compression filter. This parameter can be <b>NULL</b>.</li>
<li>The <i>pSink</i> parameter specifies the filter at the end of the chain. Typically, this filter is either a renderer for preview, or a mux for file capture.</li>
</ul>
The method connects <i>pSource</i> to <i>pIntermediate</i>, and then connects <i>pIntermediate</i> to <i>pSink</i>. If <i>pIntermediate</i> is <b>NULL</b>, the method just connects <i>pSource</i> to <i>pSink</i>. All of the filters specified by <i>pSource</i>, <i>pIntermediate</i>, and <i>pSink</i> must be added to the graph prior to calling the method. The method uses <a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>, so additional filters such as decoders might be added to the graph.

If the <i>pSink</i> parameter is <b>NULL</b>, the method tries to use a default renderer. For video it uses the <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a>, and for audio it uses the <a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a>.

If <i>pSource</i> is a filter, the method searches for an output pin on that filter. In that case, use the <i>pCategory</i> and <i>pType</i> parameters to narrow the search. For example, if a filter has separate pins for preview and capture, you can specify either PIN_CATEGORY_CAPTURE or PIN_CATEGORY_PREVIEW. If <i>pSource</i> is an output pin, set the <i>pCategory</i> and <i>pType</i> to <b>NULL</b>.

In all cases, the method searches for unconnected pins. If more than one pin meets the specified criteria, the method uses the first such pin that it finds.

Note that for DV capture, if the media type is MEDIATYPE_Interleaved and the <i>pSink</i> parameter is <b>NULL</b>, the method splits the interleaved stream into an audio stream and a video stream, and renders both of those streams.

The <code>RenderStream</code> method handles many of the details required for capture graphs:

<b>Smart Tee</b>. Some capture filters have a capture pin but no preview pin. To preview, the capture pin must be connected to the <a href="/windows/desktop/DirectShow/smart-tee-filter">Smart Tee Filter</a>. This filter splits the data into two streams, a capture stream and a preview stream. When you specify PIN_CATEGORY_PREVIEW or PIN_CATEGORY_CAPTURE, the method inserts a Smart Tee filter if one is needed. Then it renders the specified stream on the Smart Tee filter. If you render a preview stream and the method uses a Smart Tee filter, it returns VFW_S_NOPREVIEWPIN.

<b>Closed Captioning</b>. You can use this method to capture or preview closed captioning. Some capture filters deliver Vertical Blanking Interval (VBI) data, others deliver closed captioning data. To handle either case, call the method twice, once using PIN_CATEGORY_VBI and once using PIN_CATEGORY_CC. The method inserts any filters needed to convert VBI data to closed captioning. To preview the data, set the <i>pSink</i> parameter to <b>NULL</b>. To capture the data to a file, use the multiplexer filter's <b>IBaseFilter</b> interface pointer. You can capture and preview the data in the same graph. Call the method once using <b>NULL</b> and again using the multiplexer. Set the <i>pIntermediate</i> parameter to <b>NULL</b>.

<b>Video Port Pins</b>. Filters that work with video port extension (VPE) video capture hardware might have video port pins (PIN_CATEGORY_VIDEOPORT) instead of preview pins. For preview or capture to work, a video port pin must connect to the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a>. The method handles this detail. You do not have to specify PIN_CATEGORY_VIDEOPORT. Specify PIN_CATEGORY_PREVIEW or PIN_CATEGORY_CAPTURE, and the method will connect the pin correctly. In a similar way, some filters deliver VBI data using video port pins (PIN_CATEGORY_VIDEOPORT_VBI). As with PIN_CATEGORY_VIDEOPORT, the method handles this detail. You do not have to specify PIN_CATEGORY_VIDEOPORT_VBI.

<b>Supporting Filters</b>. If a capture device uses a Windows Driver Model (WDM) driver, the graph may require certain filters upstream from the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a>, such as a <a href="/windows/desktop/DirectShow/tv-tuner-filter">TV Tuner Filter</a> or an <a href="/windows/desktop/DirectShow/analog-video-crossbar-filter">Analog Video Crossbar Filter</a>. If this method successfully renders the stream, it also inserts any WDM filters that are required in your graph. The method queries the input pins on the capture filter to determine what mediums they support, and connects them to matching filters.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
For a typical capture graph, connect the preview pin to the default renderer, with no intermediate filter:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Video: 
pBuilder-&gt;RenderStream(&amp;PIN_CATEGORY_PREVIEW, &amp;MEDIATYPE_Video, 
    pCaptureFilter, NULL, NULL); 
// Audio:
pBuilder-&gt;RenderStream(&amp;PIN_CATEGORY_PREVIEW, &amp;MEDIATYPE_Audio, 
    pCaptureFilter, NULL, NULL); 
</pre>
</td>
</tr>
</table></span></div>
Connect the capture pin to a mux filter or file writer filter, depending on what type of file you wish to output. For AVI files, use the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter. For ASF files, use the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. Typically, you will get a pointer to this filter from the <i>ppf</i> parameter of the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename">ICaptureGraphBuilder2::SetOutputFileName</a> method.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
pBuilder-&gt;SetOutputFileName(&amp;MEDIASUBTYPE_Avi, L"C:\\Example.avi", 
    &amp;ppf, &amp;pSink);
pBuilder-&gt;RenderStream(&amp;PIN_CATEGORY_CAPTURE, &amp;MEDIATYPE_Video,
    pCaptureFilter, NULL, ppf);
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="File_Sources"></a><a id="file_sources"></a><a id="FILE_SOURCES"></a>File Sources</h3>
You can use this method to transcode or recompress a file. The following discussion assumes that the file has at most one video stream and one audio stream, or else a single interleaved stream. Otherwise, the method will not work correctly.

A file source has one output pin, so set <i>pCategory</i> and <i>pType</i> to <b>NULL</b>. Call the method twice—once to render the video stream, and once to render the audio stream. The first call connects the source filter to a parser filter and renders one of the parser filter's output pins. The second call renders the parser's remaining output pin. If you are compressing one stream but not the other, make sure to specify the compressor filter in the first call. The method will automatically pick the correct stream based on the compression type.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
pBuilder-&gt;RenderStream(NULL, NULL, pSrc, pCompressor, pMux);
pBuilder-&gt;RenderStream(NULL, NULL, pSrc, NULL, pMux);
</pre>
</td>
</tr>
</table></span></div>
For a complete example, see <a href="/windows/desktop/DirectShow/recompressing-an-avi-file">Recompressing an AVI File</a>.

## -see-also

<a href="/windows/desktop/DirectShow/building-graphs-with-the-capture-graph-builder">Building Graphs with the Capture Graph Builder</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>



<a href="/windows/desktop/DirectShow/video-capture">Video Capture</a>