---
UID: NN:searchapi.ISearchLanguageSupport
title: ISearchLanguageSupport
author: windows-driver-content
description: Provides methods for accessing thesaurus information.
old-location: search\_search_ISearchLanguageSupport.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\isearchlanguagesupport.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISearchLanguageSupport, ISearchLanguageSupport interface [search], ISearchLanguageSupport interface [search], described, _search_ISearchLanguageSupport, search._search_ISearchLanguageSupport, searchapi/ISearchLanguageSupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchLanguageSupport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchLanguageSupport interface


## -description


Provides methods for accessing thesaurus information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchLanguageSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchLanguageSupport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/92508989-27d9-4703-b9cd-5f5a77aaa567">EnumerateExpandedTerms</a>
</td>
<td align="left" width="63%">
Gets an enumeration of thesaurus terms for a specified word.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90f9531b-d555-47d2-9dcc-700e63c32f8a">GetDiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Gets the sensitivity of an implemented <b>ISearchLanguageSupport</b> interface to diacritics.  A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33e13e2a-3ab8-47a9-ae89-60e6601e48ee">IsNoiseWord</a>
</td>
<td align="left" width="63%">
Checks a word against a list of words that have been excluded from indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f12e031-6328-4c07-b712-8f939b4d1e75">IsPrefixNormalized</a>
</td>
<td align="left" width="63%">
Determines whether the query token is a prefix of the document token, disregarding case, width, and (optionally) diacritics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85d51d11-afdb-4911-ac0f-81e8718c4605">LoadStemmer</a>
</td>
<td align="left" width="63%">
Retrieves an interface to the word stemmer registered for the specified LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17f60cee-38af-4adc-9945-0d2739546adc">LoadWordBreaker</a>
</td>
<td align="left" width="63%">
Retrieves an interface to the word breaker registered for the specified LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20388490-3ff9-4856-acfe-30055827473a">SetDiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether an implemented <b>ISearchLanguageSupport</b> interface is sensitive to diacritics. A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation. 

</td>
</tr>
</table> 


## -remarks



A thesaurus file contains a word and a list of words to substitute when querying. It is specific to a catalog and can be defined in more than one file.



