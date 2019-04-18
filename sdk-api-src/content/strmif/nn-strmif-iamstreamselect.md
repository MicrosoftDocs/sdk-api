---
UID: NN:strmif.IAMStreamSelect
title: IAMStreamSelect (strmif.h)
author: windows-sdk-content
description: The IAMStreamSelect interface selects from the available streams on a parser filter.
old-location: dshow\iamstreamselect.htm
tech.root: DirectShow
ms.assetid: a305e91e-f506-4bd1-b4d4-7361df89e158
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMStreamSelect, IAMStreamSelect interface [DirectShow], IAMStreamSelect interface [DirectShow],described, IAMStreamSelectInterface, dshow.iamstreamselect, strmif/IAMStreamSelect
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
 - IAMStreamSelect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMStreamSelect interface


## -description



The <code>IAMStreamSelect</code> interface selects from the available streams on a parser filter. For example, a file might contain audio streams encoded in several languages, such as English, German, and French. The application could use this interface to select which language is played.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStreamSelect</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMStreamSelect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMStreamSelect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5104ce98-5b13-409a-9226-0c089ee8bb1e">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of available streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac17a218-34a4-49aa-9b4d-cb34f3c2a5d3">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables a given stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9396d4fb-e06e-4b54-9601-fd443c81ff35">Info</a>
</td>
<td align="left" width="63%">
Retrieves information about a given stream.

</td>
</tr>
</table> 


## -remarks



The following filters implement this interface:

<ul>
<li>
<a href="https://msdn.microsoft.com/abadf37f-2876-496d-90e7-77c3475a0064">MPEG-1 Stream Splitter</a> filter</li>
<li>
<a href="https://msdn.microsoft.com/06704a5a-e7ae-4187-ae36-32512d951aaf">MPEG-2 Splitter</a> filter</li>
<li>
<a href="https://msdn.microsoft.com/9b09dd86-3c22-4565-82a0-106d5ca2e42d">SAMI (CC) Parser</a> filter</li>
</ul>


