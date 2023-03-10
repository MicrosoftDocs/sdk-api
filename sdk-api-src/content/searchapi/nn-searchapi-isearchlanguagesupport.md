---
UID: NN:searchapi.ISearchLanguageSupport
title: ISearchLanguageSupport (searchapi.h)
description: Provides methods for accessing thesaurus information.
helpviewer_keywords: ["ISearchLanguageSupport","ISearchLanguageSupport interface [search]","ISearchLanguageSupport interface [search]","described","_search_ISearchLanguageSupport","search._search_ISearchLanguageSupport","searchapi/ISearchLanguageSupport"]
old-location: search\_search_ISearchLanguageSupport.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\isearchlanguagesupport.htm
ms.date: 12/05/2018
ms.keywords: ISearchLanguageSupport, ISearchLanguageSupport interface [search], ISearchLanguageSupport interface [search],described, _search_ISearchLanguageSupport, search._search_ISearchLanguageSupport, searchapi/ISearchLanguageSupport
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchLanguageSupport
 - searchapi/ISearchLanguageSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchLanguageSupport
---

# ISearchLanguageSupport interface


## -description

Provides methods for accessing thesaurus information.

## -inheritance

The <b>ISearchLanguageSupport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchLanguageSupport</b> also has these types of members:

## -remarks

A thesaurus file contains a word and a list of words to substitute when querying. It is specific to a catalog and can be defined in more than one file.
