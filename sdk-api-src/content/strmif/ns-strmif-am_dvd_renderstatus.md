---
UID: NS:strmif.__MIDL___MIDL_itf_strmif_0000_0138_0001
title: AM_DVD_RENDERSTATUS (strmif.h)
author: windows-sdk-content
description: The AM_DVD_RENDERSTATUS structure contains codes indicating the status of DVD-Video playback. These codes are used in the IDvdGraphBuilder::RenderDvdVideoVolume method.
old-location: dshow\am_dvd_renderstatus.htm
tech.root: DirectShow
ms.assetid: 6d11332e-86db-4649-af77-2906c6cbba7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AM_DVD_RENDERSTATUS, AM_DVD_RENDERSTATUS structure [DirectShow], AM_DVD_RENDERSTATUSStructure, dshow.am_dvd_renderstatus, strmif/AM_DVD_RENDERSTATUS
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AM_DVD_RENDERSTATUS
product: Windows
targetos: Windows
req.typenames: AM_DVD_RENDERSTATUS
req.redist: 
ms.custom: 19H1
---

# AM_DVD_RENDERSTATUS structure


## -description



The AM_DVD_RENDERSTATUS structure contains codes indicating the status of DVD-Video playback. These codes are used in the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a> method.




## -struct-fields




### -field hrVPEStatus

Overlay/VPE error code. Zero indicates success; any other value is failure.


### -field bDvdVolInvalid

<b>TRUE</b> if the specified DVD volume to be played does not exist; <b>FALSE</b> otherwise.


### -field bDvdVolUnknown

<b>TRUE</b> if no DVD volume is specified or if it isn't found; <b>FALSE</b> otherwise.


### -field bNoLine21In

<b>TRUE</b> if the video decoder doesn't produce line 21 (closed captioning) data; <b>FALSE</b> otherwise.


### -field bNoLine21Out

<b>TRUE</b> if the video decoder can't be shown as closed captioning on video due to a problem with graph building; <b>FALSE</b> otherwise.


### -field iNumStreams

Number of DVD streams to render.


### -field iNumStreamsFailed

Number of streams that failed to render.


### -field dwFailedStreamsFlag

Combination of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_am_dvd_stream_flags">AM_DVD_STREAM_FLAGS</a> flags indicating which streams failed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a>
 

 

