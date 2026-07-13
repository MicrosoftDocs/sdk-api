---
UID: NF:filter.IFilter.BindRegion
title: IFilter::BindRegion (filter.h)
description: Retrieves an interface representing the specified portion of object. Currently reserved for future use.
helpviewer_keywords: ["BindRegion","BindRegion method [Indexing Service]","BindRegion method [Indexing Service]","IFilter interface","IFilter interface [Indexing Service]","BindRegion method","IFilter.BindRegion","IFilter::BindRegion","_idxs_IFilter_BindRegion","filter/IFilter::BindRegion","indexsrv.ifilter_bindregion"]
old-location: indexsrv\ifilter_bindregion.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_8bam.htm
ms.date: 12/05/2018
ms.keywords: BindRegion, BindRegion method [Indexing Service], BindRegion method [Indexing Service],IFilter interface, IFilter interface [Indexing Service],BindRegion method, IFilter.BindRegion, IFilter::BindRegion, _idxs_IFilter_BindRegion, filter/IFilter::BindRegion, indexsrv.ifilter_bindregion
req.header: filter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilter::BindRegion
 - filter/IFilter::BindRegion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Filter.h
api_name:
 - IFilter.BindRegion
---

# IFilter::BindRegion


## -description

Retrieves an interface representing the specified portion of object. Currently reserved for future use.

## -parameters

### -param origPos [in]

A <a href="/windows/desktop/api/filter/ns-filter-filterregion">FILTERREGION</a> structure that contains the position of the text.

### -param riid [in]

A reference to the requested interface identifier.

### -param ppunk [out]

A pointer to a variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppunk</i> contains the requested interface pointer.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_W_REGION_CLIPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter could not bind the entire region.

</td>
</tr>
</table>

## -remarks

If it is impossible for the <b>BindRegion</b> method to bind an interface to the specified region, return FILTER_W_REGION_CLIPPED. This situation can occur when the next such chunk is in a linked object or an embedded object. 



Not all filters are capable of supporting the <b>BindRegion</b> method in a rational way. Filters that are implemented by viewing applications will benefit the most from this method. The method is intended to be a way to pass cookies through the search engine and back to the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface implementation. 

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method is currently reserved for future use. Always return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>