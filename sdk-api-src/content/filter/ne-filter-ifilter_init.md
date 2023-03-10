---
UID: NE:filter.tagIFILTER_INIT
title: IFILTER_INIT (filter.h)
description: Flags that control the filtering process.
helpviewer_keywords: ["IFILTER_INIT","IFILTER_INIT enumeration [Indexing Service]","IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES","IFILTER_INIT_APPLY_INDEX_ATTRIBUTES","IFILTER_INIT_APPLY_OTHER_ATTRIBUTES","IFILTER_INIT_CANON_HYPHENS","IFILTER_INIT_CANON_PARAGRAPHS","IFILTER_INIT_CANON_SPACES","IFILTER_INIT_DISABLE_EMBEDDED","IFILTER_INIT_EMIT_FORMATTING","IFILTER_INIT_FILTER_AGGRESSIVE_BREAK","IFILTER_INIT_FILTER_OWNED_VALUE_OK","IFILTER_INIT_HARD_LINE_BREAKS","IFILTER_INIT_INDEXING_ONLY","IFILTER_INIT_SEARCH_LINKS","_idxs_IFILTER_INIT_enum","filter/IFILTER_INIT","filter/IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES","filter/IFILTER_INIT_APPLY_INDEX_ATTRIBUTES","filter/IFILTER_INIT_APPLY_OTHER_ATTRIBUTES","filter/IFILTER_INIT_CANON_HYPHENS","filter/IFILTER_INIT_CANON_PARAGRAPHS","filter/IFILTER_INIT_CANON_SPACES","filter/IFILTER_INIT_DISABLE_EMBEDDED","filter/IFILTER_INIT_EMIT_FORMATTING","filter/IFILTER_INIT_FILTER_AGGRESSIVE_BREAK","filter/IFILTER_INIT_FILTER_OWNED_VALUE_OK","filter/IFILTER_INIT_HARD_LINE_BREAKS","filter/IFILTER_INIT_INDEXING_ONLY","filter/IFILTER_INIT_SEARCH_LINKS","indexsrv.ifilter_init_enum","tagIFILTER_INIT"]
old-location: indexsrv\ifilter_init_enum.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9dm5.htm
ms.date: 12/05/2018
ms.keywords: IFILTER_INIT, IFILTER_INIT enumeration [Indexing Service], IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, IFILTER_INIT_CANON_HYPHENS, IFILTER_INIT_CANON_PARAGRAPHS, IFILTER_INIT_CANON_SPACES, IFILTER_INIT_DISABLE_EMBEDDED, IFILTER_INIT_EMIT_FORMATTING, IFILTER_INIT_FILTER_AGGRESSIVE_BREAK, IFILTER_INIT_FILTER_OWNED_VALUE_OK, IFILTER_INIT_HARD_LINE_BREAKS, IFILTER_INIT_INDEXING_ONLY, IFILTER_INIT_SEARCH_LINKS, _idxs_IFILTER_INIT_enum, filter/IFILTER_INIT, filter/IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, filter/IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, filter/IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, filter/IFILTER_INIT_CANON_HYPHENS, filter/IFILTER_INIT_CANON_PARAGRAPHS, filter/IFILTER_INIT_CANON_SPACES, filter/IFILTER_INIT_DISABLE_EMBEDDED, filter/IFILTER_INIT_EMIT_FORMATTING, filter/IFILTER_INIT_FILTER_AGGRESSIVE_BREAK, filter/IFILTER_INIT_FILTER_OWNED_VALUE_OK, filter/IFILTER_INIT_HARD_LINE_BREAKS, filter/IFILTER_INIT_INDEXING_ONLY, filter/IFILTER_INIT_SEARCH_LINKS, indexsrv.ifilter_init_enum, tagIFILTER_INIT
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
req.typenames: IFILTER_INIT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIFILTER_INIT
 - filter/tagIFILTER_INIT
 - IFILTER_INIT
 - filter/IFILTER_INIT
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - IFILTER_INIT
---

# IFILTER_INIT enumeration


## -description

<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href=" http://www.microsoft.com/en-us/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

Flags that control the filtering process.

## -enum-fields

### -field IFILTER_INIT_CANON_PARAGRAPHS:1

Paragraph breaks should be marked with the Unicode PARAGRAPH SEPARATOR (0x2029).

### -field IFILTER_INIT_HARD_LINE_BREAKS:2

Soft returns, such as the newline character in Word, should be replaced by hard returns?LINE SEPARATOR (0x2028). Existing hard returns can be doubled. A carriage return (0x000D), line feed (0x000A), or the carriage return and line feed in combination should be considered a hard return. The intent is to enable pattern-expression matches that match against observed line breaks.

### -field IFILTER_INIT_CANON_HYPHENS:4

Various word-processing programs have forms of hyphens that are not represented in the host character set, such as optional hyphens (appearing only at the end of a line) and nonbreaking hyphens. This flag indicates that optional hyphens are to be converted to nulls, and non-breaking hyphens are to be converted to normal hyphens (0x2010), or HYPHEN-MINUSES (0x002D).

### -field IFILTER_INIT_CANON_SPACES:8

Just as the IFILTER_INIT_CANON_HYPHENS flag standardizes hyphens, this one standardizes spaces. All special space characters, such as nonbreaking spaces, are converted to the standard space character (0x0020).

### -field IFILTER_INIT_APPLY_INDEX_ATTRIBUTES:16

Indicates that the client wants text split into chunks representing internal value-type properties.

### -field IFILTER_INIT_APPLY_OTHER_ATTRIBUTES:32

Any properties not covered by the IFILTER_INIT_APPLY_INDEX_ATTRIBUTES and IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES flags should be emitted.

### -field IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES:256

Indicates that the client wants text split into chunks representing properties determined during the indexing process.

### -field IFILTER_INIT_INDEXING_ONLY:64

Optimizes <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> for indexing because the client calls the <a href="/windows/desktop/api/filter/nf-filter-ifilter-init">IFilter::Init</a> method only once and does not call <a href="/windows/desktop/api/filter/nf-filter-ifilter-bindregion">IFilter::BindRegion</a>. This eliminates the possibility of accessing a chunk both before and after accessing another chunk.

### -field IFILTER_INIT_SEARCH_LINKS:128

The text extraction process must recursively search all linked objects within the document. If a link is unavailable, the <a href="/windows/desktop/api/filter/nf-filter-ifilter-getchunk">IFilter::GetChunk</a> call that would have obtained the first chunk of the link should return FILTER_E_LINK_UNAVAILABLE.

### -field IFILTER_INIT_FILTER_OWNED_VALUE_OK:512

The content indexing process can return property values set by the filter.

### -field IFILTER_INIT_FILTER_AGGRESSIVE_BREAK:1024

TBD

### -field IFILTER_INIT_DISABLE_EMBEDDED:2048

TBD

### -field IFILTER_INIT_EMIT_FORMATTING:4096

TBD

## -remarks

Generally, text output by the <a href="/windows/desktop/api/filter/nf-filter-ifilter-gettext">IFilter::GetText</a> method should match exactly the actual text of the document. However, in order to achieve maximum interoperability, some standardization of common features is desirable. These features include paragraph breaks, line breaks, hyphens and spaces. <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface servers can also embed null characters in text, which are nearly ignored by clients. That is, Unicode character 0x0000 is completely ignored and 0x0001 is treated as a word break.

Four flags control text standardization: IFILTER_INIT_CANON_PARAGRAPHS, IFILTER_INIT_HARD_LINE_BREAKS, IFILTER_INIT_CANON_HYPHENS, and IFILTER_INIT_CANON_SPACES.

Different clients of the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface want different views of an object. Three flags, IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, and IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, control the set of properties that should be applied to chunks. In addition, specific properties can be requested in calls to the <a href="/windows/desktop/api/filter/nf-filter-ifilter-init">IFilter::Init</a> method as an array of size cAttributes, stored in aAttributes.




<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface implementations need to store some chunk information when operations other than content indexing occur. IFILTER_INIT_INDEXING_ONLY optimizes the filter for indexing.

For viewing purposes, it can be desirable to search across links as well as in the document and any objects it embeds. IFILTER_INIT_SEARCH_LINKS specifies recursively searching all links.

Certain <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface implementations might generate property values during the content indexing process, and IFILTER_INIT_FILTER_OWNED_VALUE_OK indicates that it is OK to return these values.

## -see-also

<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>
