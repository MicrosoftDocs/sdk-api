---
UID: NE:strmif._AM_DVD_GRAPH_FLAGS
title: "_AM_DVD_GRAPH_FLAGS"
author: windows-sdk-content
description: The AM_DVD_GRAPH_FLAGS enumeration specifies how the DVD Navigator builds a DVD playback graph. These flags are used with the IDvdGraphBuilder::RenderDvdVideoVolume method.
old-location: dshow\am_dvd_graph_flags.htm
old-project: DirectShow
ms.assetid: 2a0ec036-d34c-407e-9b6d-c3bd3881a0af
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: AM_DVD_DO_NOT_CLEAR, AM_DVD_EVR_ONLY, AM_DVD_GRAPH_FLAGS, AM_DVD_GRAPH_FLAGS , AM_DVD_GRAPH_FLAGS enumeration [DirectShow], AM_DVD_GRAPH_FLAGSEnumeration, AM_DVD_HWDEC_ONLY, AM_DVD_HWDEC_PREFER, AM_DVD_NOVPE, AM_DVD_SWDEC_ONLY, AM_DVD_SWDEC_PREFER, AM_DVD_VMR9_ONLY, _AM_DVD_GRAPH_FLAGS, dshow.am_dvd_graph_flags, strmif/AM_DVD_DO_NOT_CLEAR, strmif/AM_DVD_EVR_ONLY, strmif/AM_DVD_GRAPH_FLAGS, strmif/AM_DVD_HWDEC_ONLY, strmif/AM_DVD_HWDEC_PREFER, strmif/AM_DVD_NOVPE, strmif/AM_DVD_SWDEC_ONLY, strmif/AM_DVD_SWDEC_PREFER, strmif/AM_DVD_VMR9_ONLY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: AM_DVD_GRAPH_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	AM_DVD_GRAPH_FLAGS
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# _AM_DVD_GRAPH_FLAGS enumeration


## -description



The <b>AM_DVD_GRAPH_FLAGS</b> enumeration specifies how the DVD Navigator builds a DVD playback graph. These flags are used with the <a href="https://msdn.microsoft.com/731d2f4b-2a54-451a-8d98-b5fdf47c1dc8">IDvdGraphBuilder::RenderDvdVideoVolume</a> method.




## -enum-fields




### -field AM_DVD_HWDEC_PREFER

Use a hardware decoder if possible. If none is available, use a software decoder. This is the default setting. Hardware DVD decoders are registered under the CLSID_DVDHWDecodersCategory filter category. See <a href="https://msdn.microsoft.com/cab4e2c9-eab9-4836-adfc-870490ca5b6b">Filter Categories</a>.


### -field AM_DVD_HWDEC_ONLY

Use a hardware decoder; do not use a software decoder. Do not combine this flag with the AM_DVD_VMR9_ONLY or AM_DVD_EVR_ONLY flag.


### -field AM_DVD_SWDEC_PREFER

Use a software decoder if possible. If none is available, use a hardware decoder.


### -field AM_DVD_SWDEC_ONLY

Use a software decoder; do not use a hardware decoder.


### -field AM_DVD_NOVPE

Do not show video on the computer monitor. Use of this flag should be limited only to the combination of a hardware DVD-Video decoder and a display device with a port that can connect to a TV. A set-top box type of device that can play back DVD-Video could play DVD titles to be viewed on a TV set rather than a computer monitor.


### -field AM_DVD_DO_NOT_CLEAR

Do not clear the filter graph before building the DVD playback graph. By default, the <a href="https://msdn.microsoft.com/731d2f4b-2a54-451a-8d98-b5fdf47c1dc8">RenderDvdVideoVolume</a> method removes any existing filters from the graph before it builds the DVD playback graph. <div class="alert"><b>Note</b>  Applies to Windows Vista and later.</div>
<div> </div>



### -field AM_DVD_VMR9_ONLY

Use the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9) for rendering; fail if the VMR-9 is not available. Do not combine this flag with the AM_DVD_EVR_ONLY flag.


### -field AM_DVD_EVR_ONLY

Use the Enhanced Video Renderer (EVR) for rendering; fail if the EVR is not available. <div class="alert"><b>Note</b>  Applies to Windows Vista and later.</div>
<div> </div>



### -field AM_DVD_EVR_QOS


### -field AM_DVD_ADAPT_GRAPH


### -field AM_DVD_MASK




## -remarks



Do not combine more than one of the following flags:

<ul>
<li>AM_DVD_HWDEC_PREFER</li>
<li>AM_DVD_HWDEC_ONLY</li>
<li>AM_DVD_SWDEC_PREFER</li>
<li>AM_DVD_SWDEC_ONLY</li>
</ul>
If you have already selected a video renderer by calling <a href="https://msdn.microsoft.com/e16cb767-87a9-49f6-a3a7-88166f2abe73">IDvdGraphBuilder::GetDvdInterface</a>, do not set the <b>AM_DVD_VMR9_ONLY</b> or <b>AM_DVD_EVR_ONLY</b> flag.

To use the VMR-9, the decoder's <a href="https://msdn.microsoft.com/727db98f-96a1-4fe1-8315-0280541817c2">IAMDecoderCaps::GetDecoderCaps</a> method must return the <b>AM_GETDECODERCAP_QUERY_VMR9_SUPPORT</b> flag. To use the EVR, the decoder's <b>GetDecoderCaps</b> method must return the <b>AM_GETDECODERCAP_QUERY_EVR_SUPPORT</b> flag.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/731d2f4b-2a54-451a-8d98-b5fdf47c1dc8">IDvdGraphBuilder::RenderDvdVideoVolume</a>
 

 

