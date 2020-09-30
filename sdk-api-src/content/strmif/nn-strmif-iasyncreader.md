---
UID: NN:strmif.IAsyncReader
title: IAsyncReader (strmif.h)
description: The IAsyncReader interface performs an asynchronous data request on a filter.This interface is exposed by output pins that perform asynchronous read operations.
helpviewer_keywords: ["IAsyncReader","IAsyncReader interface [DirectShow]","IAsyncReader interface [DirectShow]","described","IAsyncReaderInterface","dshow.iasyncreader","strmif/IAsyncReader"]
old-location: dshow\iasyncreader.htm
tech.root: dshow
ms.assetid: 54a18567-e9d4-4b12-b486-cdd70d719184
ms.date: 12/05/2018
ms.keywords: IAsyncReader, IAsyncReader interface [DirectShow], IAsyncReader interface [DirectShow],described, IAsyncReaderInterface, dshow.iasyncreader, strmif/IAsyncReader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAsyncReader
 - strmif/IAsyncReader
dev_langs:
 - c++
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
---

# IAsyncReader interface


## -description

The <code>IAsyncReader</code> interface performs an asynchronous data request on a filter.

This interface is exposed by output pins that perform asynchronous read operations. The interface is used by the input pin on the downstream filter. Applications do not use this interface. The <a href="/windows/desktop/DirectShow/file-source--async--filter">Async File Source</a> filter exposes this interface on its output pin.

<b>Filter developers</b>: Implement this interface if your output pin delivers data in the form of a byte stream (MEDIATYPE_Stream) and supports the pull model. During the connection process, check whether the downstream pin queries for the <code>IAsyncReader</code> interface. If it does not, your pin should either fail the connection or establish some other transport. (If your pin derives from <a href="/windows/desktop/DirectShow/cbasepin">CBasePin</a>, perform this check in the <a href="/windows/desktop/DirectShow/cbasepin-checkconnect">CBasePin::CheckConnect</a> method.)

For more information about using this interface, see the following topics:

<ul>
<li>
<a href="/windows/desktop/DirectShow/negotiating-allocators">Negotiating Allocators</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/data-flow-for-filter-developers">Data Flow for Filter Developers</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/cpullpin">CPullPin Class</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAsyncReader</b> also has these types of members:
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
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-beginflush">BeginFlush</a>
</td>
<td align="left" width="63%">
Causes all outstanding reads to return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-endflush">EndFlush</a>
</td>
<td align="left" width="63%">
Ends the flushing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-length">Length</a>
</td>
<td align="left" width="63%">
Retrieves the total length of the stream, and the currently available length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">Request</a>
</td>
<td align="left" width="63%">
Queues a request for data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-requestallocator">RequestAllocator</a>
</td>
<td align="left" width="63%">
Retrieves the actual allocator to be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-syncread">SyncRead</a>
</td>
<td align="left" width="63%">
Performs a synchronized read.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-syncreadaligned">SyncReadAligned</a>
</td>
<td align="left" width="63%">
Performs an aligned synchronized read.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-waitfornext">WaitForNext</a>
</td>
<td align="left" width="63%">
Blocks until the next sample is completed or the time-out occurs.

</td>
</tr>
</table>