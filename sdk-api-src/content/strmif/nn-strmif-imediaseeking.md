---
UID: NN:strmif.IMediaSeeking
title: IMediaSeeking
author: windows-sdk-content
description: The IMediaSeeking interface contains methods for seeking to a position within a stream, and for setting the playback rate.
old-location: dshow\imediaseeking.htm
tech.root: DirectShow
ms.assetid: 32adad53-d1ac-495f-9347-7bdd4ae4b78d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaSeeking, IMediaSeeking interface [DirectShow], IMediaSeeking interface [DirectShow],described, IMediaSeekingInterface, dshow.imediaseeking, strmif/IMediaSeeking
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSeeking interface


## -description



The <code>IMediaSeeking</code> interface contains methods for seeking to a position within a stream, and for setting the playback rate. The Filter Graph Manager exposes this interface, and so do individual filters or pins. Applications should query the Filter Graph Manager for the interface.

The Filter Graph Manager distributes any <code>IMediaSeeking</code> call to each of the renderer filters in the graph. The renderer filters send the call upstream to the source filters. This sequence of events ensures that all streams remain synchronized. If any of the distributed calls returns an error, the Filter Graph Manager returns the first error value it received, even if some of the distributed calls succeed. An exception is E_NOTIMPL: the Filter Graph Manager does not return E_NOTIMPL unless it was returned by all of the distributed calls.

An application can seek the graph while the graph is in any state (running, paused or stopped). If the graph is running, the Filter Graph Manager pauses the graph before it issues the seek command. Then it runs the graph again. All seeking operations are independent of the current playback rate. Seeking operations cause any pending media data to be flushed from the graph.

For all <code>IMediaSeeking</code> parameters that specify time, the unit of time depends on the current time format. To set the time format, call the <a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a> method. Time formats are globally unique identifiers (GUIDs) defined in uuids.h. For more information, see <a href="https://msdn.microsoft.com/510c7146-ff3c-4812-a7ad-b4051aa82ef3">Time Format GUIDs</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaSeeking</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaSeeking</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d0062f66-213d-4f91-9f73-780be39ee432">CheckCapabilities</a>
</td>
<td align="left" width="63%">
Queries whether a stream has specified seeking capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/868ec03e-d4e5-4a1e-914a-6be8933f1c7c">ConvertTimeFormat</a>
</td>
<td align="left" width="63%">
Converts from one time format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c4114e5-ff82-421a-a7fb-9382d4182388">GetAvailable</a>
</td>
<td align="left" width="63%">
Gets the range of times in which seeking is efficient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84dd3c21-9c72-4433-bd03-29520dc138ca">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves all the seeking capabilities of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dca0c9e-ce95-4716-8e4d-ce8bf83628d6">GetCurrentPosition</a>
</td>
<td align="left" width="63%">
Gets the current position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15b98fb0-a0dd-47fc-8046-fa336afa970c">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b267c02-ec2d-4251-aac7-f2f711b16062">GetPositions</a>
</td>
<td align="left" width="63%">
Gets the current position and the stop position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d519aab-eb35-4a00-b6fe-23d734f969ae">GetPreroll</a>
</td>
<td align="left" width="63%">
Gets the amount of data that will be queued before the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/419b223d-95b9-4df6-8b65-56846faa6afe">GetRate</a>
</td>
<td align="left" width="63%">
Gets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7205ea09-65c1-4cd5-b76d-55977b0fbab9">GetStopPosition</a>
</td>
<td align="left" width="63%">
Gets the time at which the playback will stop, relative to the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa6dc75e-f124-4404-b8fd-ef227d8cada0">GetTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the time format that is currently being used for seek operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/443a8dbc-c12a-4d50-9005-1fedf701f6fd">IsFormatSupported</a>
</td>
<td align="left" width="63%">
Determines whether a specified time format is supported for seek operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27211946-9b05-40fc-823e-efad87a730a3">IsUsingTimeFormat</a>
</td>
<td align="left" width="63%">
Determines whether seek operations are currently using a specified time format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16fd71d6-c162-493c-9bca-479d59da5031">QueryPreferredFormat</a>
</td>
<td align="left" width="63%">
Gets the preferred time format for seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa1369fd-a57a-4246-bb23-969f6ce3cad8">SetPositions</a>
</td>
<td align="left" width="63%">
Sets the current position and the stop position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cd44480-cadb-4b59-9fe7-4a82b3aed15b">SetRate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">SetTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the time format for subsequent seek operations.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/525605c8-cffa-4b2c-bd2f-eb02d3ff3e95">Seeking the Filter Graph</a>
 

 

