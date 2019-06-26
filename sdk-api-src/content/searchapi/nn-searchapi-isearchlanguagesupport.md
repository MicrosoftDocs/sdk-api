---
UID: NN:searchapi.ISearchLanguageSupport
title: ISearchLanguageSupport (searchapi.h)
author: windows-sdk-content
description: Provides methods for accessing thesaurus information.
old-location: search\_search_ISearchLanguageSupport.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\isearchlanguagesupport.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchLanguageSupport, ISearchLanguageSupport interface [search], ISearchLanguageSupport interface [search],described, _search_ISearchLanguageSupport, search._search_ISearchLanguageSupport, searchapi/ISearchLanguageSupport
ms.topic: interface
f1_keywords: 
 - "searchapi/ISearchLanguageSupport"
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchlanguagesupport.idl
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
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchLanguageSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchLanguageSupport interface


## -description


Provides methods for accessing thesaurus information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchLanguageSupport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchLanguageSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchLanguageSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb266438(v=vs.85)">EnumerateExpandedTerms</a>
</td>
<td align="left" width="63%">
Gets an enumeration of thesaurus terms for a specified word.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchlanguagesupport-getdiacriticsensitivity">GetDiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Gets the sensitivity of an implemented <b>ISearchLanguageSupport</b> interface to diacritics.  A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb266441(v=vs.85)">IsNoiseWord</a>
</td>
<td align="left" width="63%">
Checks a word against a list of words that have been excluded from indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchlanguagesupport-isprefixnormalized">IsPrefixNormalized</a>
</td>
<td align="left" width="63%">
Determines whether the query token is a prefix of the document token, disregarding case, width, and (optionally) diacritics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchlanguagesupport-loadstemmer">LoadStemmer</a>
</td>
<td align="left" width="63%">
Retrieves an interface to the word stemmer registered for the specified LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchlanguagesupport-loadwordbreaker">LoadWordBreaker</a>
</td>
<td align="left" width="63%">
Retrieves an interface to the word breaker registered for the specified LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchlanguagesupport-setdiacriticsensitivity">SetDiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether an implemented <b>ISearchLanguageSupport</b> interface is sensitive to diacritics. A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation. 

</td>
</tr>
</table> 


## -remarks



A thesaurus file contains a word and a list of words to substitute when querying. It is specific to a catalog and can be defined in more than one file.



