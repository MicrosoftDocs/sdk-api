---
UID: NN:control.IMediaPosition
title: IMediaPosition
author: windows-sdk-content
description: The IMediaPosition interface contains methods for seeking to a position within a stream.
old-location: dshow\imediaposition.htm
tech.root: DirectShow
ms.assetid: 325dd9a4-80ca-43e3-9ff8-473df1b833e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaPosition, IMediaPosition interface [DirectShow], IMediaPosition interface [DirectShow],described, IMediaPositionInterface, control/IMediaPosition, dshow.imediaposition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: control.h
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
 - IMediaPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaPosition interface


## -description



The <b>IMediaPosition</b> interface contains methods for seeking to a position within a stream. 


<div class="alert"><b>Note</b>  Applications should use <a href="https://msdn.microsoft.com/en-us/library/Dd407023(v=VS.85).aspx">IMediaSeeking</a> instead of <b>IMediaPosition</b>. </div>
<div> </div>


This interface is exposed by the Filter Graph Manager as well as by individual filters. Applications should obtain an <b>IMediaPosition</b> interface pointer from the Filter Graph Manager, not from a filter. The Filter Graph Manager distributes method calls to all of the renderer filters. The renderer filters propagate the calls upstream to the source filters. This sequence of events ensures that all streams remain synchronized.

If one of the distributed calls returns an error, the Filter Graph Manager returns the first error value it received. Some of the distributed calls may have succeeded in this case. However, the filter graph does not return <b>E_NOTIMPL</b> unless all the distributed calls return <b>E_NOTIMPL</b>. If at least one filter in the graph implements the method, the Filter Graph Manager does not return <b>E_NOTIMPL</b>.






## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaPosition</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMediaPosition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaPosition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406978(v=VS.85).aspx">CanSeekBackward</a>
</td>
<td align="left" width="63%">
Determines whether the filter graph can seek backward in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406980(v=VS.85).aspx">CanSeekForward</a>
</td>
<td align="left" width="63%">
Determines whether the filter graph can seek forward in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406984(v=VS.85).aspx">get_CurrentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406985(v=VS.85).aspx">get_Duration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406986(v=VS.85).aspx">get_PrerollTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of data that will be queued before the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406987(v=VS.85).aspx">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406988(v=VS.85).aspx">get_StopTime</a>
</td>
<td align="left" width="63%">
Retrieves the time at which the playback will stop, relative to the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406991(v=VS.85).aspx">put_CurrentPosition</a>
</td>
<td align="left" width="63%">
Sets the current position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406992(v=VS.85).aspx">put_PrerollTime</a>
</td>
<td align="left" width="63%">
Sets the amount of data that will be queued before the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406993(v=VS.85).aspx">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406994(v=VS.85).aspx">put_StopTime</a>
</td>
<td align="left" width="63%">
Sets the time at which the playback will stop, relative to the duration of the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

