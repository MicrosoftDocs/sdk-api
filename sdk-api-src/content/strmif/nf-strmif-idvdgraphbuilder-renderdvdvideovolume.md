---
UID: NF:strmif.IDvdGraphBuilder.RenderDvdVideoVolume
title: IDvdGraphBuilder::RenderDvdVideoVolume (strmif.h)
description: The RenderDvdVideoVolume method completes building a filter graph according to user specifications for playing a DVD-Video volume.
helpviewer_keywords: ["IDvdGraphBuilder interface [DirectShow]","RenderDvdVideoVolume method","IDvdGraphBuilder.RenderDvdVideoVolume","IDvdGraphBuilder::RenderDvdVideoVolume","IDvdGraphBuilderRenderDvdVideoVolume","RenderDvdVideoVolume","RenderDvdVideoVolume method [DirectShow]","RenderDvdVideoVolume method [DirectShow]","IDvdGraphBuilder interface","dshow.idvdgraphbuilder_renderdvdvideovolume","strmif/IDvdGraphBuilder::RenderDvdVideoVolume"]
old-location: dshow\idvdgraphbuilder_renderdvdvideovolume.htm
tech.root: DirectShow
ms.assetid: 731d2f4b-2a54-451a-8d98-b5fdf47c1dc8
ms.date: 12/05/2018
ms.keywords: IDvdGraphBuilder interface [DirectShow],RenderDvdVideoVolume method, IDvdGraphBuilder.RenderDvdVideoVolume, IDvdGraphBuilder::RenderDvdVideoVolume, IDvdGraphBuilderRenderDvdVideoVolume, RenderDvdVideoVolume, RenderDvdVideoVolume method [DirectShow], RenderDvdVideoVolume method [DirectShow],IDvdGraphBuilder interface, dshow.idvdgraphbuilder_renderdvdvideovolume, strmif/IDvdGraphBuilder::RenderDvdVideoVolume
f1_keywords:
- strmif/IDvdGraphBuilder.RenderDvdVideoVolume
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdGraphBuilder.RenderDvdVideoVolume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdGraphBuilder::RenderDvdVideoVolume


## -description



The <code>RenderDvdVideoVolume</code> method completes building a filter graph according to user specifications for playing a DVD-Video volume.




## -parameters




### -param lpcwszPathName [in]

Pointer to the path for the DVD-Video volume to play. Can be <b>NULL</b>.


### -param dwFlags [in]

Bitwise OR of flags from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-am_dvd_graph_flags">AM_DVD_GRAPH_FLAGS</a> enumeration, specifying how to build the DVD playback graph.


### -param pStatus [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_dvd_renderstatus">AM_DVD_RENDERSTATUS</a> structure. When the method returns, the structure indicates any rendering failures.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation return values include the following:

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
The <i>dwFlags</i> parameter specifies conflicting options.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method partially succeeded. To find out which errors occurred, examine the <i>pStatus</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, and all streams were rendered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_DECNOTENOUGH</b></dt>
</dl>
</td>
<td width="60%">
One or more streams could not be rendered.

If you specified the AM_DVD_HWDEC_ONLY or AM_DVD_SWDEC_ONLY flag in the <i>dwFlags</i> parameter, try calling the method again with the AM_DVD_HWDEC_PREFER or AM_DVD_SWDEC_PREFER flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NON_EVR_RENDERER_IN_FILTER_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The filter graph already contains a video renderer. The method returns this error code if you specify the AM_DVD_EVR_ONLY flag in the <i>dwFlags</i> parameter but the graph already contains a video renderer other than the Enhanced Video Renderer (VMR) filter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_RENDERFAIL</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while building the graph. For example, the DVD Graph Builder could not create a required filter or could not render any of the streams.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_TOO_MANY_RENDERERS_IN_FILTER_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The filter graph contains more than one video renderer.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_dvd_renderstatus">AM_DVD_RENDERSTATUS</a> structure reflects failure codes for this method. Reasons for this method returning S_FALSE include the following:

<ul>
<li>The graph has been completely built, but one of the following is true.<ul>
<li>Overlay mixing doesn't work—the application did not set the AM_DVD_NOVPE flag and the video stream could not be put through the Overlay Mixer. In this case, if the video is decoded in software the application will have enough information to inform the user that the video won't be visible. Hardware-decoded video will be visible only on a TV connected to the NTSC out port of the hardware video decoder.</li>
<li>The video decoder does not produce line 21 data. The application can display a warning or informative message that closed captioning is not available because of the decoder.</li>
<li>No volume path is specified and the DVD Navigator did not locate any DVD-Video volume to be played. The application can ask the user to insert a DVD-Video disc if none is available in the drive when playback starts.</li>
</ul>
</li>
<li>Some streams did not render. The application can indicate to the user that some streams can't be played.</li>
</ul>
This method builds the graph without any knowledge of the DVD-Video file or volume to play. The DVD-Video graph builder builds the graph even if <i>lpcwszPathName</i> is <b>NULL</b> or if the DVD Navigator filter does not find a default DVD-Video volume to play.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdgraphbuilder">IDvdGraphBuilder Interface</a>
 

 

