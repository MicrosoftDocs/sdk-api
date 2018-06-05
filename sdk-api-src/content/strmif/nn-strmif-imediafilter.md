---
UID: NN:strmif.IMediaFilter
title: IMediaFilter
author: windows-sdk-content
description: The IMediaFilter interface controls the streaming state of a filter.All DirectShow filters implement this interface.
old-location: dshow\imediafilter.htm
old-project: DirectShow
ms.assetid: 5c0060e8-a9e5-4141-a38d-9a1bc55cc91b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMediaFilter, IMediaFilter interface [DirectShow], IMediaFilter interface [DirectShow],described, IMediaFilterInterface, dshow.imediafilter, strmif/IMediaFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaFilter interface


## -description



The <code>IMediaFilter</code> interface controls the streaming state of a filter.

All DirectShow filters implement this interface. It provides methods for switching the filter between states (stopped, paused, and running); for retrieving the filter's current state; and for setting a reference clock. Applications should not call <code>IMediaFilter</code> methods on filters.

The <a href="https://msdn.microsoft.com/b1a53193-27c6-4e86-a5b9-f3c1e4401690">Filter Graph Manager</a> also exposes this interface. Applications can use the <b>SetSyncSource</b> method to set the graph reference clock, and <b>GetSyncSource</b> to retrieve the clock. Applications should not call the other methods on this interface. Instead, use the corresponding methods on the <a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl</a> interface.

The <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface inherits from <code>IMediaFilter</code>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaFilter</b> interface inherits from <b>IPersist</b>. <b>IMediaFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b20ca3e9-bec2-4c6d-ba80-f4dae2f5a831">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the filter (running, stopped, or paused).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f5eb31c-3a12-45f4-9c95-caafc0267481">GetSyncSource</a>
</td>
<td align="left" width="63%">
Retrieves the current reference clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a>
</td>
<td align="left" width="63%">
Runs the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a374c963-cc28-41f6-814d-7ffc6efc67a6">SetSyncSource</a>
</td>
<td align="left" width="63%">
Sets the reference clock for the filter or the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops the filter.

</td>
</tr>
</table> 

