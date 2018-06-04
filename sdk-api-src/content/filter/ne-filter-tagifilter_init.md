---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagIFILTER_INIT enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Flags that control the filtering process.


## -enum-fields




### -field IFILTER_INIT_CANON_PARAGRAPHS

Paragraph breaks should be marked with the Unicode PARAGRAPH SEPARATOR (0x2029).


### -field IFILTER_INIT_HARD_LINE_BREAKS

Soft returns, such as the newline character in Word, should be replaced by hard returns?LINE SEPARATOR (0x2028). Existing hard returns can be doubled. A carriage return (0x000D), line feed (0x000A), or the carriage return and line feed in combination should be considered a hard return. The intent is to enable pattern-expression matches that match against observed line breaks.


### -field IFILTER_INIT_CANON_HYPHENS

Various word-processing programs have forms of hyphens that are not represented in the host character set, such as optional hyphens (appearing only at the end of a line) and nonbreaking hyphens. This flag indicates that optional hyphens are to be converted to nulls, and non-breaking hyphens are to be converted to normal hyphens (0x2010), or HYPHEN-MINUSES (0x002D).


### -field IFILTER_INIT_CANON_SPACES

Just as the IFILTER_INIT_CANON_HYPHENS flag standardizes hyphens, this one standardizes spaces. All special space characters, such as nonbreaking spaces, are converted to the standard space character (0x0020).


### -field IFILTER_INIT_APPLY_INDEX_ATTRIBUTES

Indicates that the client wants text split into chunks representing internal value-type properties.


### -field IFILTER_INIT_APPLY_OTHER_ATTRIBUTES

Any properties not covered by the IFILTER_INIT_APPLY_INDEX_ATTRIBUTES and IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES flags should be emitted.


### -field IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES

Indicates that the client wants text split into chunks representing properties determined during the indexing process.


### -field IFILTER_INIT_INDEXING_ONLY

Optimizes <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> for indexing because the client calls the <a href="https://msdn.microsoft.com/5cb9b675-258e-46b0-905f-15a086f84f74">IFilter::Init</a> method only once and does not call <a href="https://msdn.microsoft.com/d4ee07f3-4260-4b33-9ac9-436d17c80f2c">IFilter::BindRegion</a>. This eliminates the possibility of accessing a chunk both before and after accessing another chunk. 



### -field IFILTER_INIT_SEARCH_LINKS

The text extraction process must recursively search all linked objects within the document. If a link is unavailable, the <a href="https://msdn.microsoft.com/4d4f3150-deec-40b6-a945-b4cea241db8d">IFilter::GetChunk</a> call that would have obtained the first chunk of the link should return FILTER_E_LINK_UNAVAILABLE.


### -field IFILTER_INIT_FILTER_OWNED_VALUE_OK

The content indexing process can return property values set by the filter.


### -field IFILTER_INIT_FILTER_AGGRESSIVE_BREAK

TBD


### -field IFILTER_INIT_DISABLE_EMBEDDED

TBD


### -field IFILTER_INIT_EMIT_FORMATTING

TBD


## -remarks



Generally, text output by the <a href="https://msdn.microsoft.com/d63639a6-6729-44cd-8105-198a268ff2d6">IFilter::GetText</a> method should match exactly the actual text of the document. However, in order to achieve maximum interoperability, some standardization of common features is desirable. These features include paragraph breaks, line breaks, hyphens and spaces. <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> interface servers can also embed null characters in text, which are nearly ignored by clients. That is, Unicode character 0x0000 is completely ignored and 0x0001 is treated as a word break.

Four flags control text standardization: IFILTER_INIT_CANON_PARAGRAPHS, IFILTER_INIT_HARD_LINE_BREAKS, IFILTER_INIT_CANON_HYPHENS, and IFILTER_INIT_CANON_SPACES.

Different clients of the <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> interface want different views of an object. Three flags, IFILTER_INIT_APPLY_INDEX_ATTRIBUTES, IFILTER_INIT_APPLY_CRAWL_ATTRIBUTES, and IFILTER_INIT_APPLY_OTHER_ATTRIBUTES, control the set of properties that should be applied to chunks. In addition, specific properties can be requested in calls to the <a href="https://msdn.microsoft.com/5cb9b675-258e-46b0-905f-15a086f84f74">IFilter::Init</a> method as an array of size cAttributes, stored in aAttributes.




<a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> interface implementations need to store some chunk information when operations other than content indexing occur. IFILTER_INIT_INDEXING_ONLY optimizes the filter for indexing.

For viewing purposes, it can be desirable to search across links as well as in the document and any objects it embeds. IFILTER_INIT_SEARCH_LINKS specifies recursively searching all links.

Certain <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> interface implementations might generate property values during the content indexing process, and IFILTER_INIT_FILTER_OWNED_VALUE_OK indicates that it is OK to return these values.




## -see-also




<a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a>
 

 

