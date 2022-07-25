---
UID: NE:strmif._AM_DVD_GRAPH_FLAGS
title: AM_DVD_GRAPH_FLAGS (strmif.h)
description: The AM_DVD_GRAPH_FLAGS enumeration specifies how the DVD Navigator builds a DVD playback graph. These flags are used with the IDvdGraphBuilder::RenderDvdVideoVolume method.
helpviewer_keywords: ["AM_DVD_DO_NOT_CLEAR","AM_DVD_EVR_ONLY","AM_DVD_GRAPH_FLAGS","AM_DVD_GRAPH_FLAGS","AM_DVD_GRAPH_FLAGS enumeration [DirectShow]","AM_DVD_GRAPH_FLAGSEnumeration","AM_DVD_HWDEC_ONLY","AM_DVD_HWDEC_PREFER","AM_DVD_NOVPE","AM_DVD_SWDEC_ONLY","AM_DVD_SWDEC_PREFER","AM_DVD_VMR9_ONLY","dshow.am_dvd_graph_flags","strmif/AM_DVD_DO_NOT_CLEAR","strmif/AM_DVD_EVR_ONLY","strmif/AM_DVD_GRAPH_FLAGS","strmif/AM_DVD_HWDEC_ONLY","strmif/AM_DVD_HWDEC_PREFER","strmif/AM_DVD_NOVPE","strmif/AM_DVD_SWDEC_ONLY","strmif/AM_DVD_SWDEC_PREFER","strmif/AM_DVD_VMR9_ONLY"]
old-location: dshow\am_dvd_graph_flags.htm
tech.root: dshow
ms.assetid: 2a0ec036-d34c-407e-9b6d-c3bd3881a0af
ms.date: 12/05/2018
ms.keywords: AM_DVD_DO_NOT_CLEAR, AM_DVD_EVR_ONLY, AM_DVD_GRAPH_FLAGS, AM_DVD_GRAPH_FLAGS , AM_DVD_GRAPH_FLAGS enumeration [DirectShow], AM_DVD_GRAPH_FLAGSEnumeration, AM_DVD_HWDEC_ONLY, AM_DVD_HWDEC_PREFER, AM_DVD_NOVPE, AM_DVD_SWDEC_ONLY, AM_DVD_SWDEC_PREFER, AM_DVD_VMR9_ONLY, dshow.am_dvd_graph_flags, strmif/AM_DVD_DO_NOT_CLEAR, strmif/AM_DVD_EVR_ONLY, strmif/AM_DVD_GRAPH_FLAGS, strmif/AM_DVD_HWDEC_ONLY, strmif/AM_DVD_HWDEC_PREFER, strmif/AM_DVD_NOVPE, strmif/AM_DVD_SWDEC_ONLY, strmif/AM_DVD_SWDEC_PREFER, strmif/AM_DVD_VMR9_ONLY
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
req.typenames: AM_DVD_GRAPH_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_DVD_GRAPH_FLAGS
 - strmif/_AM_DVD_GRAPH_FLAGS
 - AM_DVD_GRAPH_FLAGS
 - strmif/AM_DVD_GRAPH_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AM_DVD_GRAPH_FLAGS
---

# AM_DVD_GRAPH_FLAGS enumeration


## -description

The <b>AM_DVD_GRAPH_FLAGS</b> enumeration specifies how the DVD Navigator builds a DVD playback graph. These flags are used with the <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a> method.

## -enum-fields

### -field AM_DVD_HWDEC_PREFER:0x1

Use a hardware decoder if possible. If none is available, use a software decoder. This is the default setting. Hardware DVD decoders are registered under the CLSID_DVDHWDecodersCategory filter category. See <a href="/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.

### -field AM_DVD_HWDEC_ONLY:0x2

Use a hardware decoder; do not use a software decoder. Do not combine this flag with the AM_DVD_VMR9_ONLY or AM_DVD_EVR_ONLY flag.

### -field AM_DVD_SWDEC_PREFER:0x4

Use a software decoder if possible. If none is available, use a hardware decoder.

### -field AM_DVD_SWDEC_ONLY:0x8

Use a software decoder; do not use a hardware decoder.

### -field AM_DVD_NOVPE:0x100

Do not show video on the computer monitor. Use of this flag should be limited only to the combination of a hardware DVD-Video decoder and a display device with a port that can connect to a TV. A set-top box type of device that can play back DVD-Video could play DVD titles to be viewed on a TV set rather than a computer monitor.

### -field AM_DVD_DO_NOT_CLEAR:0x200

Do not clear the filter graph before building the DVD playback graph. By default, the <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">RenderDvdVideoVolume</a> method removes any existing filters from the graph before it builds the DVD playback graph. <div class="alert"><b>Note</b>  Applies to Windows Vista and later.</div>
<div> </div>

### -field AM_DVD_VMR9_ONLY:0x800

Use the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) for rendering; fail if the VMR-9 is not available. Do not combine this flag with the AM_DVD_EVR_ONLY flag.

### -field AM_DVD_EVR_ONLY:0x1000

Use the Enhanced Video Renderer (EVR) for rendering; fail if the EVR is not available. <div class="alert"><b>Note</b>  Applies to Windows Vista and later.</div>
<div> </div>

### -field AM_DVD_EVR_QOS:0x2000

### -field AM_DVD_ADAPT_GRAPH:0x4000

### -field AM_DVD_MASK:0xffff

## -remarks

Do not combine more than one of the following flags:

<ul>
<li>AM_DVD_HWDEC_PREFER</li>
<li>AM_DVD_HWDEC_ONLY</li>
<li>AM_DVD_SWDEC_PREFER</li>
<li>AM_DVD_SWDEC_ONLY</li>
</ul>
If you have already selected a video renderer by calling <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-getdvdinterface">IDvdGraphBuilder::GetDvdInterface</a>, do not set the <b>AM_DVD_VMR9_ONLY</b> or <b>AM_DVD_EVR_ONLY</b> flag.

To use the VMR-9, the decoder's <a href="/windows/desktop/api/strmif/nf-strmif-iamdecodercaps-getdecodercaps">IAMDecoderCaps::GetDecoderCaps</a> method must return the <b>AM_GETDECODERCAP_QUERY_VMR9_SUPPORT</b> flag. To use the EVR, the decoder's <b>GetDecoderCaps</b> method must return the <b>AM_GETDECODERCAP_QUERY_EVR_SUPPORT</b> flag.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a>
