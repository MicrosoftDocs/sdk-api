---
UID: NN:control.IMediaPosition
title: IMediaPosition
author: windows-sdk-content
description: The IMediaPosition interface contains methods for seeking to a position within a stream.
old-location: dshow\imediaposition.htm
old-project: DirectShow
ms.assetid: 325dd9a4-80ca-43e3-9ff8-473df1b833e9
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMediaPosition, IMediaPosition interface [DirectShow], IMediaPosition interface [DirectShow],described, IMediaPositionInterface, control/IMediaPosition, dshow.imediaposition
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaPosition interface


## -description



The <b>IMediaPosition</b> interface contains methods for seeking to a position within a stream. 


<div class="alert"><b>Note</b>  Applications should use <a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking</a> instead of <b>IMediaPosition</b>. </div>
<div> </div>


This interface is exposed by the Filter Graph Manager as well as by individual filters. Applications should obtain an <b>IMediaPosition</b> interface pointer from the Filter Graph Manager, not from a filter. The Filter Graph Manager distributes method calls to all of the renderer filters. The renderer filters propagate the calls upstream to the source filters. This sequence of events ensures that all streams remain synchronized.

If one of the distributed calls returns an error, the Filter Graph Manager returns the first error value it received. Some of the distributed calls may have succeeded in this case. However, the filter graph does not return <b>E_NOTIMPL</b> unless all the distributed calls return <b>E_NOTIMPL</b>. If at least one filter in the graph implements the method, the Filter Graph Manager does not return <b>E_NOTIMPL</b>.






## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaPosition</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMediaPosition</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8152553a-173b-4f0b-bcdf-b9c20912921d">CanSeekBackward</a>
</td>
<td align="left" width="63%">
Determines whether the filter graph can seek backward in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0647d629-79f0-4c62-a346-8d99646469c6">CanSeekForward</a>
</td>
<td align="left" width="63%">
Determines whether the filter graph can seek forward in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96f4d621-c618-49fa-a0f6-bcc68a41467e">get_CurrentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9971ca0e-a16d-4227-9efa-c965d501e6ef">get_Duration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cfe9ba0-0138-4847-81ab-ea1e96e2c3a8">get_PrerollTime</a>
</td>
<td align="left" width="63%">
Retrieves the amount of data that will be queued before the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbe18522-6adc-4a55-b74a-db05f619d40a">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6139ebb2-fad8-4394-9a5f-4753ca9fb143">get_StopTime</a>
</td>
<td align="left" width="63%">
Retrieves the time at which the playback will stop, relative to the duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6af44ce9-91d3-4329-835a-a1249924d672">put_CurrentPosition</a>
</td>
<td align="left" width="63%">
Sets the current position, relative to the total duration of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a09e6e9f-7e6f-4e53-b805-ee4b9d97f4e7">put_PrerollTime</a>
</td>
<td align="left" width="63%">
Sets the amount of data that will be queued before the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fba6bb5a-6709-41e6-bf76-182c88ee42e3">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c068310e-4083-46ac-8ec6-3d57976f4a88">put_StopTime</a>
</td>
<td align="left" width="63%">
Sets the time at which the playback will stop, relative to the duration of the stream.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

