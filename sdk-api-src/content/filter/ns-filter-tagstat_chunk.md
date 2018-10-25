---
UID: NS:filter.tagSTAT_CHUNK
title: tagSTAT_CHUNK
author: windows-sdk-content
description: Describes the characteristics of a chunk.
old-location: search\_search_STAT_CHUNK.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\stat_chunk.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: STAT_CHUNK, STAT_CHUNK structure [search], _search_STAT_CHUNK, filter/STAT_CHUNK, search._search_STAT_CHUNK, tagSTAT_CHUNK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Filter.h
api_name:
 - STAT_CHUNK
product: Windows
targetos: Windows
req.typenames: STAT_CHUNK
req.redist: the Windows NT 4.0 Option Pack
---

# tagSTAT_CHUNK structure


## -description


Describes the characteristics of a chunk.


## -struct-fields




### -field idChunk

Type: <b>ULONG</b>

The chunk identifier. Chunk identifiers must be unique for the current instance of the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface. Chunk identifiers must be in ascending order. The order in which chunks are numbered should correspond to the order in which they appear in the source document. Some search engines can take advantage of the proximity of chunks of various properties. If so, the order in which chunks with different properties are emitted will be important to the search engine.


### -field breakType

Type: <b><a href="https://msdn.microsoft.com/f1c5b1c8-cd6c-4831-8d32-f727f710aa36">CHUNK_BREAKTYPE</a></b>

The type of break that separates the previous chunk from the current chunk. Values are from the <a href="https://msdn.microsoft.com/f1c5b1c8-cd6c-4831-8d32-f727f710aa36">CHUNK_BREAKTYPE</a> enumeration.


### -field flags

Type: <b><a href="https://msdn.microsoft.com/07a6a106-cdd3-4598-8cdb-4e37321dd43a">CHUNKSTATE</a></b>

Flags that indicate whether this chunk contains a text-type or a value-type property. Flag values are taken from the <a href="https://msdn.microsoft.com/07a6a106-cdd3-4598-8cdb-4e37321dd43a">CHUNKSTATE</a> enumeration. If the <b>CHUNK_TEXT</b> flag is set, <a href="https://msdn.microsoft.com/8a27f57a-eebe-4c72-91c6-25fc8ccc7822">IFilter::GetText</a> should be used to retrieve the contents of the chunk as a series of words. If the <b>CHUNK_VALUE</b> flag is set, <a href="https://msdn.microsoft.com/21dba344-e1a6-4a05-b68f-4fd93a2976ff">IFilter::GetValue</a> should be used to retrieve the value and it should be treated as a single property value. If the filter dictates that the same content be treated both as text and as a value, the chunk should be emitted twice in two different chunks, each with one flag set.


### -field locale

Type: <b>LCID</b>

The language and sublanguage associated with a chunk of text. Chunk locale is used by document indexers to perform proper word breaking of text. If the chunk is neither text-type nor value-type and is of data type <b>VT_LPWSTR</b>, <b>VT_LPSTR</b> or <b>VT_BSTR</b>, this field is ignored.


### -field attribute

Type: <b><a href="https://msdn.microsoft.com/f3bc90bd-5428-44f8-bd60-3fe3ee9781cb">FULLPROPSPEC</a></b>

The property to be applied to the chunk. If a filter requires that the same text have more than one property, it must emit the text once for each property in separate chunks.


### -field idChunkSource

Type: <b>ULONG</b>

The ID of the source of a chunk. The value of this member depends on the nature of the chunk:

                    

<ul>
<li>If the chunk is a text-type property, the value of this member must be the same as the value of the <b>idChunk</b> member.</li>
<li>If the chunk is an internal value-type property derived from textual content, the value of this member is the chunk ID for the text-type chunk from which it is derived.</li>
<li>If the filter attributes specify to return only internal value-type properties, there is no content chunk from which to derive the current internal value-type property. In this case, the value of this member must be set to zero, which is an invalid chunk.</li>
</ul>

### -field cwcStartSource

Type: <b>ULONG</b>

The offset at which the source text for a derived chunk starts in the source chunk.


### -field cwcLenSource

Type: <b>ULONG</b>

The length in characters of the source text from which the current chunk was derived. A zero value signifies character-by-character correspondence between the source text and the derived text. A nonzero value means that no such direct correspondence exists.


## -remarks



The final three members (<b>idChunkSource</b>, <b>cwcStartSource</b>, and <b>cwcLenSource</b>) are used to describe the source of a derived chunk; that is, a source that can be mapped back to a section of text. For example, the heading of a chapter can be both a text–type property and an internal value–type property — a heading. The value–type property "heading" would be a derived chunk. If the text of the current value–type chunk (from an internal value–type property) is derived from some text–type chunk, then it must be emitted more than once.

                

The following segment is an example of how this might happen in a book.

<code>The small detective exclaimed, "C'est fini!"</code>

<b>Confessions</b>

<code>The room was silent for several minutes. After thinking very hard about it, the young woman asked, "But how did you know?"</code>

This segment might be broken into chunks in the following way.

<table class="clsStd">
<tr>
<th>ID</th>
<th>Text</th>
<th>BreakType</th>
<th>Flags</th>
<th>Locale</th>
<th>Attribute</th>
</tr>
<tr>
<td>1</td>
<td>The small dete</td>
<td>N/A</td>
<td>CHUNK_TEXT</td>
<td>ENGLISH_UK</td>
<td>CONTENT</td>
</tr>
<tr>
<td>2</td>
<td>ctive exclaimed,</td>
<td>CHUNK_NO_
BREAK</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr>
<td>3</td>
<td>"C'est fini!"</td>
<td>CHUNK_EOW</td>
<td>CHUNK_TEXT</td>
<td>FRENCH_BELGIAN</td>
<td>CONTENT</td>
</tr>
<tr>
<td>4</td>
<td>Confessions</td>
<td>CHUNK_EOC</td>
<td>CHUNK_TEXT</td>
<td>ENGLISH_UK</td>
<td>CHAPTER_
NAMES</td>
</tr>
<tr>
<td>5</td>
<td>Confessions</td>
<td>CHUNK_EOP</td>
<td>CHUNK_TEXT</td>
<td>ENGLISH_UK</td>
<td>CONTENT</td>
</tr>
<tr>
<td>6</td>
<td>The room was silent for several minutes.</td>
<td>CHUNK_EOP</td>
<td>CHUNK_TEXT</td>
<td>ENGLISH_UK</td>
<td>CONTENT</td>
</tr>
<tr>
<td>7</td>
<td>After thinking very hard about it, the young woman asked, "But how did you know?"</td>
<td>CHUNK_EOS</td>
<td>CHUNK_TEXT</td>
<td>ENGLISH_UK</td>
<td>CONTENT</td>
</tr>
</table>
 

Information provided by <b>idChunkSource</b>, <b>cwcStartSource</b>, and <b>cwcLenSource</b> is useful for a search engine that highlights hits. If the query is done for an internal value–type property, the search engine will highlight the original text from which the text of the internal value–type property has been derived. For instance, in a C++ code filter, the browser, when searching for MyFunction in internal value–type property "function definitions," will highlight the function header in the file.




## -see-also




<a href="https://msdn.microsoft.com/07a6a106-cdd3-4598-8cdb-4e37321dd43a">CHUNKSTATE</a>



<a href="https://msdn.microsoft.com/f1c5b1c8-cd6c-4831-8d32-f727f710aa36">CHUNK_BREAKTYPE</a>



<a href="https://msdn.microsoft.com/361b0edc-579f-471a-8b4d-4ef1ae242b32">GetChunk</a>



<a href="https://msdn.microsoft.com/8a27f57a-eebe-4c72-91c6-25fc8ccc7822">GetText</a>



<a href="https://msdn.microsoft.com/21dba344-e1a6-4a05-b68f-4fd93a2976ff">GetValue</a>



<a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>



<b>Reference</b>
 

 

