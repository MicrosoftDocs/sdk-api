---
UID: NF:filter.IFilter.GetText
title: IFilter::GetText (filter.h)
description: Retrieves text (text-type properties) from the current chunk, which must have a CHUNKSTATE enumeration value of CHUNK_TEXT.
helpviewer_keywords: ["GetText","GetText method [Indexing Service]","GetText method [Indexing Service]","IFilter interface","IFilter interface [Indexing Service]","GetText method","IFilter.GetText","IFilter::GetText","_idxs_IFilter_GetText","filter/IFilter::GetText","indexsrv.ifilter_gettext"]
old-location: indexsrv\ifilter_gettext.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_5378.htm
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Indexing Service], GetText method [Indexing Service],IFilter interface, IFilter interface [Indexing Service],GetText method, IFilter.GetText, IFilter::GetText, _idxs_IFilter_GetText, filter/IFilter::GetText, indexsrv.ifilter_gettext
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
 - IFilter::GetText
 - filter/IFilter::GetText
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
 - IFilter.GetText
---

# IFilter::GetText


## -description

Retrieves text (text-type properties) from the current chunk, which must have a <a href="/windows/desktop/api/filter/ne-filter-chunkstate">CHUNKSTATE</a> enumeration value of CHUNK_TEXT.

## -parameters

### -param pcwcBuffer [in, out]

On entry, the size of <i>awcBuffer</i> array in wide/Unicode characters. On exit, the number of Unicode characters written to <i>awcBuffer</i>.

### -param awcBuffer [out]

Text retrieved from the current chunk. Do not terminate the buffer with a character. Use a null-terminated string. The null-terminated string should not exceed the size of the destination buffer.

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
<dt><b>FILTER_E_NO_TEXT 
</b></dt>
</dl>
</td>
<td width="60%">
The <b>flags</b> member of the <a href="/windows/desktop/api/filter/ns-filter-stat_chunk">STAT_CHUNK</a> structure for the current chunk does not have a value of CHUNK_TEXT. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_NO_MORE_TEXT </b></dt>
</dl>
</td>
<td width="60%">
All the text in the current chunk has been returned. Additional calls to the <a href="/windows/desktop/api/filter/nf-filter-ifilter-gettext">GetText</a> method should return this error until the <a href="/windows/desktop/api/filter/nf-filter-ifilter-getchunk">IFilter::GetChunk</a> method has been called successfully. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_S_LAST_TEXT </b></dt>
</dl>
</td>
<td width="60%">
As an optimization, the last call that returns text can return FILTER_S_LAST_TEXT, indicating that the next call to the <a href="/windows/desktop/api/filter/nf-filter-ifilter-gettext">GetText</a> method will return FILTER_E_NO_MORE_TEXT. This optimization can save time by eliminating unnecessary calls to <b>GetText</b>.

</td>
</tr>
</table>

## -remarks

If the current chunk is too large for the <i>awcBuffer</i> array, more than one call to the <b>GetText</b> method can be required to retrieve all the text in the current chunk. Each call to the <b>GetText</b> method retrieves text that immediately follows the text from the last call to the <b>GetText</b> method. The last character from one call can be in the middle of a word, and the first character in the next call would continue that word. Search engines must handle this situation.

## -see-also

<a href="/windows/desktop/api/filter/ne-filter-chunkstate">CHUNKSTATE</a>



<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>