---
UID: NN:strmif.IAsyncReader
title: IAsyncReader
author: windows-sdk-content
description: The IAsyncReader interface performs an asynchronous data request on a filter.This interface is exposed by output pins that perform asynchronous read operations.
old-location: dshow\iasyncreader.htm
old-project: DirectShow
ms.assetid: 54a18567-e9d4-4b12-b486-cdd70d719184
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAsyncReader, IAsyncReader interface [DirectShow], IAsyncReader interface [DirectShow],described, IAsyncReaderInterface, dshow.iasyncreader, strmif/IAsyncReader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAsyncReader
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAsyncReader interface


## -description



The <code>IAsyncReader</code> interface performs an asynchronous data request on a filter.

This interface is exposed by output pins that perform asynchronous read operations. The interface is used by the input pin on the downstream filter. Applications do not use this interface. The <a href="https://msdn.microsoft.com/0cf6e7ab-b1fe-42f9-b682-c5484ef48c71">Async File Source</a> filter exposes this interface on its output pin.

<b>Filter developers</b>: Implement this interface if your output pin delivers data in the form of a byte stream (MEDIATYPE_Stream) and supports the pull model. During the connection process, check whether the downstream pin queries for the <code>IAsyncReader</code> interface. If it does not, your pin should either fail the connection or establish some other transport. (If your pin derives from <a href="https://msdn.microsoft.com/23b9a0e2-24fe-4ff9-b2bb-97630c237de9">CBasePin</a>, perform this check in the <a href="https://msdn.microsoft.com/511a1594-f3f8-4725-afcd-f14f3a4ebf20">CBasePin::CheckConnect</a> method.)

For more information about using this interface, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/fe13477c-1a7b-4098-9d0f-c54783102bc9">Negotiating Allocators</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cc7378c8-e268-4caa-98eb-6dc9c3b5bcad">Data Flow for Filter Developers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33a6c342-3896-41f8-b32d-01db3eed003e">CPullPin Class</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAsyncReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAsyncReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29153592-dbc1-42b4-bd4e-2f1aef8d4c19">BeginFlush</a>
</td>
<td align="left" width="63%">
Causes all outstanding reads to return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38a7fd8a-c027-49fd-8f52-49ddf072fe02">EndFlush</a>
</td>
<td align="left" width="63%">
Ends the flushing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e583ade-92a9-4853-96fb-c46cd24dd7ac">Length</a>
</td>
<td align="left" width="63%">
Retrieves the total length of the stream, and the currently available length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">Request</a>
</td>
<td align="left" width="63%">
Queues a request for data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bde850e-662f-4610-bac3-914c93584b30">RequestAllocator</a>
</td>
<td align="left" width="63%">
Retrieves the actual allocator to be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21806449-97b1-4890-9182-a1244c21ba30">SyncRead</a>
</td>
<td align="left" width="63%">
Performs a synchronized read.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/862511f1-7580-44db-aed5-3dd8279dcc33">SyncReadAligned</a>
</td>
<td align="left" width="63%">
Performs an aligned synchronized read.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc54f917-3b86-4c0b-b356-217bc9793504">WaitForNext</a>
</td>
<td align="left" width="63%">
Blocks until the next sample is completed or the time-out occurs.

</td>
</tr>
</table> 

