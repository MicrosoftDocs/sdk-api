---
UID: NN:tapi3if.ITMultiTrackTerminal
title: ITMultiTrackTerminal (tapi3if.h)
author: windows-sdk-content
description: This ITMultiTrackTerminal interface is exposed on all multitrack terminals. The interface includes methods for enumerating, creating, and removing tracks. The ITMultiTrackTerminal interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itmultitrackterminal.htm
tech.root: Tapi
ms.assetid: c9e5d8a4-78a6-4449-9c11-c780e72ab925
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITMultiTrackTerminal, ITMultiTrackTerminal interface [TAPI 2.2], ITMultiTrackTerminal interface [TAPI 2.2],described, _tapi3_itmultitrackterminal, tapi3.itmultitrackterminal, tapi3if/ITMultiTrackTerminal
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITMultiTrackTerminal"
dev_langs:
 - c++
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMultiTrackTerminal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMultiTrackTerminal interface


## -description


This 
<b>ITMultiTrackTerminal</b> interface is exposed on all multitrack terminals. The interface includes methods for enumerating, creating, and removing tracks. The 
<b>ITMultiTrackTerminal</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMultiTrackTerminal</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITMultiTrackTerminal</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmultitrackterminal-createtrackterminal">CreateTrackTerminal</a>
</td>
<td align="left" width="63%">
Creates a multitrack terminal that can handle a given media type or types and media direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmultitrackterminal-enumeratetrackterminals">EnumerateTrackTerminals</a>
</td>
<td align="left" width="63%">
Creates and returns an enumeration containing the terminals contained by the multitrack terminal on which this method was called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmultitrackterminal-get_directionsinuse">get_DirectionsInUse</a>
</td>
<td align="left" width="63%">
Returns the direction of all tracks managed currently by the multitrack terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmultitrackterminal-get_mediatypesinuse">get_MediaTypesInUse</a>
</td>
<td align="left" width="63%">
Returns the media types of all tracks managed currently by the multitrack terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmultitrackterminal-get_trackterminals">get_TrackTerminals</a>
</td>
<td align="left" width="63%">
Creates and returns a collection containing the terminals contained by the multitrack terminal on which this method was called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmultitrackterminal-removetrackterminal">RemoveTrackTerminal</a>
</td>
<td align="left" width="63%">
Removes the specified terminal from the collection of track terminals that belong to the multitrack terminal on which the function was called.

</td>
</tr>
</table> 

