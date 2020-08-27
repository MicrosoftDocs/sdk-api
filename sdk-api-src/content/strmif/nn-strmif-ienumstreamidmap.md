---
UID: NN:strmif.IEnumStreamIdMap
title: IEnumStreamIdMap (strmif.h)
description: The IEnumStreamIdMap interface is implemented on a standard COM collection of Stream ID maps that have been created by the MPEG-2 Demultiplexer's IMPEG2StreamIdMap::MapStreamId method.
helpviewer_keywords: ["IEnumStreamIdMap","IEnumStreamIdMap interface [DirectShow]","IEnumStreamIdMap interface [DirectShow]","described","IEnumStreamIdMapInterface","dshow.ienumstreamidmap","strmif/IEnumStreamIdMap"]
old-location: dshow\ienumstreamidmap.htm
tech.root: dshow
ms.assetid: 8bca9255-2bc8-408b-9127-e3fe050fcf01
ms.date: 12/05/2018
ms.keywords: IEnumStreamIdMap, IEnumStreamIdMap interface [DirectShow], IEnumStreamIdMap interface [DirectShow],described, IEnumStreamIdMapInterface, dshow.ienumstreamidmap, strmif/IEnumStreamIdMap
f1_keywords:
- strmif/IEnumStreamIdMap
dev_langs:
- c++
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
- IEnumStreamIdMap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumStreamIdMap interface


## -description



The <code>IEnumStreamIdMap</code> interface is implemented on a standard COM collection of Stream ID maps that have been created by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a>'s <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-impeg2streamidmap-mapstreamid">IMPEG2StreamIdMap::MapStreamId</a> method. To obtain a pointer to this interface, use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-impeg2streamidmap-enumstreamidmap">IMPEG2StreamIdMap::EnumStreamIdMap</a> method. Typically, an output pin will never have more than one stream ID mapped to it at any given time. This collection represents a snapshot of the Stream IDs mapped at the time the collection is created. The collection is not updated automatically.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumStreamIdMap</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumStreamIdMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumStreamIdMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumstreamidmap-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection and all its sub-objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumstreamidmap-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumstreamidmap-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves the iterator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumstreamidmap-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified element in the collection.

</td>
</tr>
</table> 

