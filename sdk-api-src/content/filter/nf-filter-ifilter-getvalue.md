---
UID: NF:filter.IFilter.GetValue
title: IFilter::GetValue (filter.h)
description: Retrieves a value (internal value-type property) from a chunk, which must have a CHUNKSTATE enumeration value of CHUNK_VALUE.
helpviewer_keywords: ["GetValue","GetValue method [Indexing Service]","GetValue method [Indexing Service]","IFilter interface","IFilter interface [Indexing Service]","GetValue method","IFilter.GetValue","IFilter::GetValue","_idxs_IFilter_GetValue","filter/IFilter::GetValue","indexsrv.ifilter_getvalue"]
old-location: indexsrv\ifilter_getvalue.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_1cpx.htm
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Indexing Service], GetValue method [Indexing Service],IFilter interface, IFilter interface [Indexing Service],GetValue method, IFilter.GetValue, IFilter::GetValue, _idxs_IFilter_GetValue, filter/IFilter::GetValue, indexsrv.ifilter_getvalue
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
 - IFilter::GetValue
 - filter/IFilter::GetValue
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
 - IFilter.GetValue
---

# IFilter::GetValue


## -description

Retrieves a value (internal value-type property) from a chunk, which must have a <a href="/windows/desktop/api/filter/ne-filter-chunkstate">CHUNKSTATE</a> enumeration value of CHUNK_VALUE.

## -parameters

### -param ppPropValue [out]

A pointer to an output variable that receives a pointer to the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the value-type property.

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
<dt><b>FILTER_E_NO_MORE_VALUES </b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/filter/nf-filter-ifilter-getvalue">GetValue</a> method has already been called on this chunk; this value should be returned until the <a href="/windows/desktop/api/filter/nf-filter-ifilter-getchunk">IFilter::GetChunk</a> method has been called successfully and has advanced to the next chunk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_NO_VALUES</b></dt>
</dl>
</td>
<td width="60%">
The current chunk does not have a <a href="/windows/desktop/api/filter/ne-filter-chunkstate">CHUNKSTATE</a> enumeration value of CHUNK_VALUE. 

</td>
</tr>
</table>

## -remarks

Call the <b>GetValue</b> method only once per chunk. 



Note that the effect of producing the same value from more than one chunk is undefined. Only the last setting of the value is valid.



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Allocate the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Some <b>PROPVARIANT</b> structures contain pointers, which can be freed by calling the <a href="/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a> function. It is up to the caller of the <b>GetValue</b> method to call <b>PropVariantClear</b>.

## -see-also

<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>