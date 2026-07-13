---
UID: NF:strmif.IDvdGraphBuilder.GetDvdInterface
title: IDvdGraphBuilder::GetDvdInterface (strmif.h)
description: The GetDvdInterface method retrieves interfaces from the DVD-Video playback graph to make DVD-Video playback development easier.
helpviewer_keywords: ["GetDvdInterface","GetDvdInterface method [DirectShow]","GetDvdInterface method [DirectShow]","IDvdGraphBuilder interface","IDvdGraphBuilder interface [DirectShow]","GetDvdInterface method","IDvdGraphBuilder.GetDvdInterface","IDvdGraphBuilder::GetDvdInterface","IDvdGraphBuilderGetDvdInterface","dshow.idvdgraphbuilder_getdvdinterface","strmif/IDvdGraphBuilder::GetDvdInterface"]
old-location: dshow\idvdgraphbuilder_getdvdinterface.htm
tech.root: dshow
ms.assetid: e16cb767-87a9-49f6-a3a7-88166f2abe73
ms.date: 4/26/2023
ms.keywords: GetDvdInterface, GetDvdInterface method [DirectShow], GetDvdInterface method [DirectShow],IDvdGraphBuilder interface, IDvdGraphBuilder interface [DirectShow],GetDvdInterface method, IDvdGraphBuilder.GetDvdInterface, IDvdGraphBuilder::GetDvdInterface, IDvdGraphBuilderGetDvdInterface, dshow.idvdgraphbuilder_getdvdinterface, strmif/IDvdGraphBuilder::GetDvdInterface
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
 - IDvdGraphBuilder::GetDvdInterface
 - strmif/IDvdGraphBuilder::GetDvdInterface
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
 - IDvdGraphBuilder.GetDvdInterface
---

# IDvdGraphBuilder::GetDvdInterface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDvdInterface</b> method retrieves interfaces from the DVD-Video playback graph to make DVD-Video playback development easier.

## -parameters

### -param riid [in]

IID of the requested interface.

### -param ppvIF [out]

Receives a pointer to the interface. The application must release the interface.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppvIF</i> parameter is invalid. This parameter must not be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface could not be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_GRAPHNOTREADY</b></dt>
</dl>
</td>
<td width="60%">
The graph is not built yet. See Remarks.

</td>
</tr>
</table>

## -remarks

You can use this method to select and configure a video renderer filter before you build the filter graph for DVD playback. The following interfaces are available:

<ul>
<li><b>Overlay Mixer Filter</b>: <a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo</a>.</li>
<li><b>Video Mixing Renderer 7 (VMR-7)</b>: <a href="/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig</a>, <a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap</a>, <a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl</a>, and <a href="/windows/desktop/api/strmif/nn-strmif-ivmrmonitorconfig">IVMRMonitorConfig</a>.</li>
<li><b>Video Mixing Renderer 9 (VMR-9)</b>: <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9</a>, <a href="/previous-versions/ms787059(v=vs.85)">IVMRMixerBitmap9</a>, <a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9</a>, and <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9">IVMRMonitorConfig9</a>.</li>
<li><b>Enhanced Video Renderer (EVR)</b>: <a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a> and <a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer">IMFVideoRenderer</a>.<b>Windows Server 2003, Windows XP and Windows 2000:  </b>This interface is not supported.

</li>
</ul>
If you call <b>GetDvdInterface</b> to get any of these interfaces before you build the filter graph, the DVD Graph Builder creates the appropriate video renderer. It will use this renderer later when you build the graph. After the video renderer has been selected, you can no longer retrieve the interfaces for the other video renderers. (The <b>GetDvdInterface</b> method will return E_NOINTERFACE.)

Before the DVD playback graph is built, if you request any interfaces that are not on the previous list, the method returns VFW_E_DVD_GRAPHNOTREADY. To build the DVD graph, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a>. After you build the graph, you can use <b>GetDvdInterface</b> to retrieve some additional interfaces:

<ul>
<li>
<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl</a> (deprecated), <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a>, <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo</a> (deprecated), and <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> to control DVD playback.</li>
<li>
<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow</a>, <a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo</a>, and <a href="/windows/desktop/api/control/nn-control-ibasicvideo2">IBasicVideo2</a> to control the video settings, in windowed mode only.</li>
<li>
<a href="/windows/desktop/api/control/nn-control-ibasicaudio">IBasicAudio</a> to control the audio settings.</li>
<li>
<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder</a> to control closed caption display.</li>
<li>
<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a> and <a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig2">IMixerPinConfig2</a> to configure the Overlay Mixer filter's first input pin, which delivers the primary video stream. (To get this interface for the other pins on the Overlay Mixer, enumerate the filter's pins and query them directly.) New applications should avoid using the Overlay Mixer filter.</li>
</ul>
To get other interfaces, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-getfiltergraph">IDvdGraphBuilder::GetFiltergraph</a>. Query the returned <b>IGraphBuilder</b> interface or use <b>EnumFilters</b> to enumerate the filters.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdgraphbuilder">IDvdGraphBuilder Interface</a>