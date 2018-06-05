---
UID: NN:strmif.IMPEG2StreamIdMap
title: IMPEG2StreamIdMap
author: windows-sdk-content
description: This interface is implemented on each output pin of the MPEG-2 Demultiplexer filter (Demux) and is used in program stream mode only.
old-location: dshow\impeg2streamidmap.htm
old-project: DirectShow
ms.assetid: 714c6b0e-3885-4026-8a83-06b37cc97d7c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMPEG2StreamIdMap, IMPEG2StreamIdMap interface [DirectShow], IMPEG2StreamIdMap interface [DirectShow],described, IMPEG2StreamIdMapInterface, dshow.impeg2streamidmap, strmif/IMPEG2StreamIdMap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	IMPEG2StreamIdMap
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMPEG2StreamIdMap interface


## -description



This interface is implemented on each output pin of the <a href="https://msdn.microsoft.com/99bfc55d-6519-4e85-98ce-cad27bd71ffb">MPEG-2 Demultiplexer</a> filter (Demux) and is used in program stream mode only. It is called by applications or other filters to associate the pin with a specified Stream ID and to inform the pin whether substream filtering is required on the stream. This interface is not exposed when the filter is playing back a file (pull-mode).

For transport streams, use the <a href="https://msdn.microsoft.com/45c09a02-7da8-460a-9a64-f012c2181b94">IMPEG2PIDMap</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2StreamIdMap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMPEG2StreamIdMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2StreamIdMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c42f042-c9fb-4cb9-90bb-4050a61b18da">EnumStreamIdMap</a>
</td>
<td align="left" width="63%">
Returns a collection of all the mapped Stream IDs on this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e74a1e62-1bc4-43e1-9017-85012b2ece01">MapStreamId</a>
</td>
<td align="left" width="63%">
Maps the Stream ID of an elementary stream within an MPEG-2 program stream to a media content type and substream filtering information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99e28b85-effd-4f86-b2da-ec02a05dde40">UnmapStreamId</a>
</td>
<td align="left" width="63%">
Unmaps the Stream ID mapping created in a previous call to <b>MapStreamId</b>.

</td>
</tr>
</table> 

