---
UID: NN:strmif.IEnumFilters
title: IEnumFilters (strmif.h)
description: The IEnumFilters interface enumerates the filters in a filter graph.helpviewer_keywords: ["IEnumFilters","IEnumFilters interface [DirectShow]","IEnumFilters interface [DirectShow]","described","IEnumFiltersInterface","dshow.ienumfilters","strmif/IEnumFilters"]
old-location: dshow\ienumfilters.htm
tech.root: DirectShow
ms.assetid: e105ccff-86c6-45d5-aead-6d303d038e5a
ms.date: 12/05/2018
ms.keywords: IEnumFilters, IEnumFilters interface [DirectShow], IEnumFilters interface [DirectShow],described, IEnumFiltersInterface, dshow.ienumfilters, strmif/IEnumFilters
f1_keywords:
- strmif/IEnumFilters
dev_langs:
- c++
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
- IEnumFilters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumFilters interface


## -description



The <code>IEnumFilters</code> interface enumerates the filters in a filter graph. To obtain this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-enumfilters">IFilterGraph::EnumFilters</a> method on the Filter Graph Manager. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object.

If the set of filters in the graph changes, some methods on this interface return VFW_E_ENUM_OUT_OF_SYNC. Call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumfilters-reset">IEnumFilters::Reset</a> method to resynchronize the enumerator.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFilters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumFilters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumFilters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumfilters-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumfilters-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of filters in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumfilters-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumfilters-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of filters.

</td>
</tr>
</table> 

