---
UID: NF:filter.IFilter.GetChunk
title: IFilter::GetChunk (filter.h)
description: Positions the filter at the beginning of the next chunk, or at the first chunk if this is the first call to the GetChunk method, and returns a description of the current chunk.
helpviewer_keywords: ["GetChunk","GetChunk method [Indexing Service]","GetChunk method [Indexing Service]","IFilter interface","IFilter interface [Indexing Service]","GetChunk method","IFilter.GetChunk","IFilter::GetChunk","_idxs_IFilter_GetChunk","filter/IFilter::GetChunk","indexsrv.ifilter_getchunk"]
old-location: indexsrv\ifilter_getchunk.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_96gb.htm
ms.date: 12/05/2018
ms.keywords: GetChunk, GetChunk method [Indexing Service], GetChunk method [Indexing Service],IFilter interface, IFilter interface [Indexing Service],GetChunk method, IFilter.GetChunk, IFilter::GetChunk, _idxs_IFilter_GetChunk, filter/IFilter::GetChunk, indexsrv.ifilter_getchunk
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
 - IFilter::GetChunk
 - filter/IFilter::GetChunk
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
 - IFilter.GetChunk
---

# IFilter::GetChunk


## -description

Positions the filter at the beginning of the next chunk, or at the first chunk if this is the first call to the <b>GetChunk</b> method, and returns a description of the current chunk.

## -parameters

### -param pStat [out]

A pointer to a <a href="/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a> structure containing a description of the current chunk.

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
<dt><b>FILTER_E_END_OF_CHUNKS</b></dt>
</dl>
</td>
<td width="60%">
The previous chunk is the last chunk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_EMBEDDING_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The next chunk is an embedding and no content filter is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_LINK_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The next chunk is a link and no content filter is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
Password or other security-related access failure. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_ACCESS </b></dt>
</dl>
</td>
<td width="60%">
General access failure.

</td>
</tr>
</table>

## -remarks

If upon return <i>pStat</i> points to a <a href="/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a> structure with the <b>breakType</b> member equal to CHUNK_NO_BREAK, only the <b>idChunk</b> member will be updated with the new chunk identifier (ID) value. The other members of the <b>STAT_CHUNK</b> structure remain unchanged. 



Internal value-type properties (chunks with a <a href="/windows/desktop/api/filter/ne-filter-chunkstate">CHUNKSTATE</a> enumeration value of CHUNK_VALUE) cannot be concatenated using CHUNK_NO_BREAK. A single word cannot span more than two glued chunks. 



Chunk ID zero is invalid.



Before the <b>GetChunk</b> method is called for the first time, there is no current chunk. After an error return code of anything other than FILTER_E_END_OF_CHUNKS the next call to the <b>GetChunk</b> method nevertheless retrieves the next chunk after the unavailable one.



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When the <b>GetChunk</b> method finishes, the chunk described in *<i>pStat</i> is the current chunk. The chunk descriptor is owned by the routine calling the <b>GetChunk</b> method, but the property name pointer, which can be set in the property specification, is owned by the <b>GetChunk</b> method and should not be freed. 



<h3><a id="Notes_to_Implementers_"></a><a id="notes_to_implementers_"></a><a id="NOTES_TO_IMPLEMENTERS_"></a>Notes to Implementers
</h3>
If a call to the <b>GetChunk</b> method of the content filter of a linked or embedded object returns FILTER_E_END_OF_CHUNKS, the implementation should return the next chunk of the linking or embedding object. For example, if a document has two embedded objects and the first has returned FILTER_E_END_OF_CHUNKS, then the outer content filter must call the <b>GetChunk</b> method of the content filter for the embedded object.



Before returning the results of a call to the <b>GetChunk</b> method on an embedded or linked object, check to make sure that the chunk ID is unique. If not, the implementer must renumber the chunk and keep a mapping of the new chunk ID.

## -see-also

<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>



<a href="/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a>