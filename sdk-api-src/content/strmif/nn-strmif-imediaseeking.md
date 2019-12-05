---
UID: NN:strmif.IMediaSeeking
title: IMediaSeeking (strmif.h)
description: The IMediaSeeking interface contains methods for seeking to a position within a stream, and for setting the playback rate.
old-location: dshow\imediaseeking.htm
tech.root: DirectShow
ms.assetid: 32adad53-d1ac-495f-9347-7bdd4ae4b78d
ms.date: 12/05/2018
ms.keywords: IMediaSeeking, IMediaSeeking interface [DirectShow], IMediaSeeking interface [DirectShow],described, IMediaSeekingInterface, dshow.imediaseeking, strmif/IMediaSeeking
ms.topic: interface
f1_keywords:
- strmif/IMediaSeeking
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
- IMediaSeeking
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSeeking interface


## -description



The <code>IMediaSeeking</code> interface contains methods for seeking to a position within a stream, and for setting the playback rate. The Filter Graph Manager exposes this interface, and so do individual filters or pins. Applications should query the Filter Graph Manager for the interface.

The Filter Graph Manager distributes any <code>IMediaSeeking</code> call to each of the renderer filters in the graph. The renderer filters send the call upstream to the source filters. This sequence of events ensures that all streams remain synchronized. If any of the distributed calls returns an error, the Filter Graph Manager returns the first error value it received, even if some of the distributed calls succeed. An exception is E_NOTIMPL: the Filter Graph Manager does not return E_NOTIMPL unless it was returned by all of the distributed calls.

An application can seek the graph while the graph is in any state (running, paused or stopped). If the graph is running, the Filter Graph Manager pauses the graph before it issues the seek command. Then it runs the graph again. All seeking operations are independent of the current playback rate. Seeking operations cause any pending media data to be flushed from the graph.

For all <code>IMediaSeeking</code> parameters that specify time, the unit of time depends on the current time format. To set the time format, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method. Time formats are globally unique identifiers (GUIDs) defined in uuids.h. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaSeeking</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaSeeking</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaSeeking</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-checkcapabilities">CheckCapabilities</a>
</td>
<td align="left" width="63%">
Queries whether a stream has specified seeking capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-converttimeformat">ConvertTimeFormat</a>
</td>
<td align="left" width="63%">
Converts from one time format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getavailable">GetAvailable</a>
</td>
<td align="left" width="63%">
Gets the range of times in which seeking is efficient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves all the seeking capabilities of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcurrentposition">GetCurrentPosition</a>
</td>
<td align="left" width="63%">
Gets the current position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getpositions">GetPositions</a>
</td>
<td align="left" width="63%">
Gets the current position and the stop position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getpreroll">GetPreroll</a>
</td>
<td align="left" width="63%">
Gets the amount of data that will be queued before the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getrate">GetRate</a>
</td>
<td align="left" width="63%">
Gets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-getstopposition">GetStopPosition</a>
</td>
<td align="left" width="63%">
Gets the time at which the playback will stop, relative to the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-gettimeformat">GetTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the time format that is currently being used for seek operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-isformatsupported">IsFormatSupported</a>
</td>
<td align="left" width="63%">
Determines whether a specified time format is supported for seek operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-isusingtimeformat">IsUsingTimeFormat</a>
</td>
<td align="left" width="63%">
Determines whether seek operations are currently using a specified time format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-querypreferredformat">QueryPreferredFormat</a>
</td>
<td align="left" width="63%">
Gets the preferred time format for seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-setpositions">SetPositions</a>
</td>
<td align="left" width="63%">
Sets the current position and the stop position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-setrate">SetRate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">SetTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the time format for subsequent seek operations.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/seeking-the-filter-graph">Seeking the Filter Graph</a>
 

 

