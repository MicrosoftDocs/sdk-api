---
UID: NE:filter.tagIFILTER_INIT
title: tagIFILTER_INIT
author: windows-sdk-content
description: Contains flags that control:
old-location: search\_search_IFILTER_INIT_ENUM.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\ifilter_init.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IFILTER_INIT, IFILTER_INIT enumeration [search], IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, IFILTER_INIT_CANON_HYPHENS, IFILTER_INIT_CANON_PARAGRAPHS, IFILTER_INIT_CANON_SPACES, IFILTER_INIT_DISABLED_EMBEDDED, IFILTER_INIT_EMIT_FORMATTING, IFILTER_INIT_FILTER_AGGRESSIVE_BREAK, IFILTER_INIT_FILTER_OWNED_VALUE_OK, IFILTER_INIT_HARD_LINE_BREAKS, IFILTER_INIT_INDEXING_ONLY, IFILTER_INIT_SEARCH_LINKS, _search_IFILTER_INIT, filter/IFILTER_INIT, filter/IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, filter/IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, filter/IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, filter/IFILTER_INIT_CANON_HYPHENS, filter/IFILTER_INIT_CANON_PARAGRAPHS, filter/IFILTER_INIT_CANON_SPACES, filter/IFILTER_INIT_DISABLED_EMBEDDED, filter/IFILTER_INIT_EMIT_FORMATTING, filter/IFILTER_INIT_FILTER_AGGRESSIVE_BREAK, filter/IFILTER_INIT_FILTER_OWNED_VALUE_OK, filter/IFILTER_INIT_HARD_LINE_BREAKS, filter/IFILTER_INIT_INDEXING_ONLY, filter/IFILTER_INIT_SEARCH_LINKS, search._search_IFILTER_INIT_ENUM, tagIFILTER_INIT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: filter.h
req.include-header: 
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
 - IFILTER_INIT
product: Windows
targetos: Windows
req.typenames: IFILTER_INIT
req.redist: 
---

# tagIFILTER_INIT enumeration


## -description


Contains flags that control:
<ul>
<li>Mapping of nonprinting character codes</li>
<li>Property output </li>
<li>Embedding scope </li>
<li>
<a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> access patterns</li>
</ul>The <a href="https://msdn.microsoft.com/c0ec3db9-23c4-449e-8106-572c432ea7cc">Init</a>method uses these flags to control the filtering process.


## -enum-fields




### -field IFILTER_INIT_CANON_PARAGRAPHS

Paragraph breaks should be marked with the Unicode PARAGRAPH SEPARATOR (0x2029).


### -field IFILTER_INIT_HARD_LINE_BREAKS

Soft returns, such as the newline character in Word, should be replaced by hard returns?LINE SEPARATOR (0x2028). Existing hard returns can be doubled. A carriage return (0x000D), line feed (0x000A), or the carriage return and line feed in combination should be considered a hard return. The intent is to enable pattern-expression matching against observed line breaks.


### -field IFILTER_INIT_CANON_HYPHENS

Various word-processing programs have forms of hyphens that are not represented in the host character set, such as optional hyphens (appearing only at the end of a line) and nonbreaking hyphens. This flag indicates that optional hyphens are to be converted to nulls, and non-breaking hyphens are to be converted to normal hyphens (0x2010), or HYPHEN-MINUSES (0x002D).


### -field IFILTER_INIT_CANON_SPACES

All special space characters, such as nonbreaking spaces, are converted to the standard space character (0x0020). 


### -field IFILTER_INIT_APPLY_INDEX_ATTRIBUTES

The client requires that text is split into chunks that represent internal value-type properties.


### -field IFILTER_INIT_APPLY_OTHER_ATTRIBUTES

Any properties not covered by the IFILTER_INIT_APPLY_INDEX_ATTRIBUTES and IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES flags should be emitted.


### -field IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES

The client wants text split into chunks representing properties determined during the indexing process.


### -field IFILTER_INIT_INDEXING_ONLY

 The client  calls the <a href="https://msdn.microsoft.com/c0ec3db9-23c4-449e-8106-572c432ea7cc">Init</a>method only once, optimizing <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> for indexing. 


### -field IFILTER_INIT_SEARCH_LINKS

The text extraction process must recursively search all linked objects within the document. If a link is unavailable, the <a href="https://msdn.microsoft.com/361b0edc-579f-471a-8b4d-4ef1ae242b32">GetChunk</a>call that would have obtained the first chunk of the link should return FILTER_E_LINK_UNAVAILABLE.


### -field IFILTER_INIT_FILTER_OWNED_VALUE_OK

The content indexing process can return property values set by the filter.


### -field IFILTER_INIT_FILTER_AGGRESSIVE_BREAK

Text should be broken in chunks more aggressively than normal. 


### -field IFILTER_INIT_DISABLE_EMBEDDED


### -field IFILTER_INIT_EMIT_FORMATTING

The <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> should emit formatting info.


#### - IFILTER_INIT_DISABLED_EMBEDDED

The <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> should not return chunks from embedded content. 


## -remarks



Generally, text output by the  <a href="https://msdn.microsoft.com/8a27f57a-eebe-4c72-91c6-25fc8ccc7822">GetText</a>method should match exactly the actual text of the document. However, to achieve maximum interoperability, some common features should be standardized. These features include paragraph breaks, line breaks, hyphens, and spaces. <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface servers can also embed null characters in text, which are nearly ignored by clients. That is, Unicode character 0x0000 is completely ignored and 0x0001 is treated as a word break.

Four flags control text standardization: IFILTER_INIT_CANON_PARAGRAPHS, IFILTER_INIT_HARD_LINE_BREAKS, IFILTER_INIT_CANON_HYPHENS, and IFILTER_INIT_CANON_SPACES.

Different clients of the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface require different views of an object. Three flags, IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, and IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, control the set of properties that should be applied to chunks. In addition, specific properties can be requested as an array of size <i>cAttributes</i>, stored in <i>aAttributes</i> in calls to the <a href="https://msdn.microsoft.com/c0ec3db9-23c4-449e-8106-572c432ea7cc">Init</a>method.


<a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface implementations need to store some chunk information when operations other than content indexing occur. IFILTER_INIT_INDEXING_ONLY optimizes the filter for indexing.

For viewing purposes, it can be desirable to search across links and in the document and any objects embedded in it. IFILTER_INIT_SEARCH_LINKS specifies that all links are searched recursively.

Certain <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface implementations might generate property values during the content indexing process, and IFILTER_INIT_FILTER_OWNED_VALUE_OK indicates that it is okay to return these values.



