---
UID: NN:sbe.ISBE2StreamMap
title: ISBE2StreamMap (sbe.h)
author: windows-sdk-content
description: Handles the mapping between output pins and streams for the Stream Buffer Source filter.
old-location: mstv\isbe2streammap.htm
tech.root: mstv
ms.assetid: d63691ca-2420-4c54-b343-be85d634488c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISBE2StreamMap, ISBE2StreamMap interface [Microsoft TV Technologies], ISBE2StreamMap interface [Microsoft TV Technologies],described, mstv.isbe2streammap, sbe/ISBE2StreamMap
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2StreamMap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISBE2StreamMap interface


## -description


Handles the mapping between output pins and streams for the <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter.

This interface is implemented by the  output pins  of the Stream Buffer Source filter. To get a pointer to the interface, query the output pin.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2StreamMap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISBE2StreamMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2StreamMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb98db94-3aa1-4f29-b98a-7594e27466ef">EnumMappedStreams</a>
</td>
<td align="left" width="63%">
Enumerates all SBE2 streams that are mapped to filter output pins.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">MapStream</a>
</td>
<td align="left" width="63%">
Maps an SBE2 stream to an output pin.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75736e65-b708-4162-836d-7694899d23d7">UnmapStream</a>
</td>
<td align="left" width="63%">
Removes the mapping between an SBE2 stream and an output pin.


</td>
</tr>
</table> 


## -remarks



In version 1 of the Stream Buffer Engine (SBE), each output pin is mapped to a single stream for the lifetime of the filter. Starting in version 2 of SBE,   the application can change the mapping, as follows:

<ol>
<li>Query the Stream Buffer Source filter for the <a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a> interface.</li>
<li>Disable default stream mode by calling the <a href="https://msdn.microsoft.com/5038050b-319d-488a-9cea-a2fc59b90cc8">ISBE2Crossbar::EnableDefaultMode</a> method without the DEF_MODE_STREAMS flag.</li>
<li>Query the output pin for the <b>ISBE2StreamMap</b> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">ISBE2StreamMap::MapStream</a>.</li>
</ol>
    For more information, see <a href="https://msdn.microsoft.com/af6262c5-391c-4248-9f96-26bd108b0fdf">Stream Buffer Source Filter Enhancements in Windows 7</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2StreamMap)</code>.



