---
UID: NN:tapi3if.ITMultiTrackTerminal
title: ITMultiTrackTerminal
author: windows-sdk-content
description: This ITMultiTrackTerminal interface is exposed on all multitrack terminals. The interface includes methods for enumerating, creating, and removing tracks. The ITMultiTrackTerminal interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itmultitrackterminal.htm
old-project: tapi
ms.assetid: c9e5d8a4-78a6-4449-9c11-c780e72ab925
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITMultiTrackTerminal, ITMultiTrackTerminal interface [TAPI 2.2], ITMultiTrackTerminal interface [TAPI 2.2],described, _tapi3_itmultitrackterminal, tapi3.itmultitrackterminal, tapi3if/ITMultiTrackTerminal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMultiTrackTerminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMultiTrackTerminal interface


## -description


This 
<b>ITMultiTrackTerminal</b> interface is exposed on all multitrack terminals. The interface includes methods for enumerating, creating, and removing tracks. The 
<b>ITMultiTrackTerminal</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMultiTrackTerminal</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITMultiTrackTerminal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMultiTrackTerminal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe853de7-5a22-4b49-aca0-e2e2a8c3e1d7">CreateTrackTerminal</a>
</td>
<td align="left" width="63%">
Creates a multitrack terminal that can handle a given media type or types and media direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90ef12f5-1a94-49ca-85c3-092306503827">EnumerateTrackTerminals</a>
</td>
<td align="left" width="63%">
Creates and returns an enumeration containing the terminals contained by the multitrack terminal on which this method was called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9f739ea-3df5-4275-868a-3e0d611254c0">get_DirectionsInUse</a>
</td>
<td align="left" width="63%">
Returns the direction of all tracks managed currently by the multitrack terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c2ebbba-66a4-4ef0-abba-faab129e64e2">get_MediaTypesInUse</a>
</td>
<td align="left" width="63%">
Returns the media types of all tracks managed currently by the multitrack terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bedefe8-6b84-48c0-8a7b-719d017baf24">get_TrackTerminals</a>
</td>
<td align="left" width="63%">
Creates and returns a collection containing the terminals contained by the multitrack terminal on which this method was called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59f257ef-9e52-40fb-a72c-732105262016">RemoveTrackTerminal</a>
</td>
<td align="left" width="63%">
Removes the specified terminal from the collection of track terminals that belong to the multitrack terminal on which the function was called.

</td>
</tr>
</table> 

