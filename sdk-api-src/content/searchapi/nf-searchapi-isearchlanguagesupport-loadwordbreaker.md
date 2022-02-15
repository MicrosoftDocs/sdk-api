---
UID: NF:searchapi.ISearchLanguageSupport.LoadWordBreaker
title: ISearchLanguageSupport::LoadWordBreaker (searchapi.h)
description: Retrieves an interface to the word breaker registered for the specified language code identifier (LCID).
helpviewer_keywords: ["ISearchLanguageSupport interface [search]","LoadWordBreaker method","ISearchLanguageSupport.LoadWordBreaker","ISearchLanguageSupport::LoadWordBreaker","LoadWordBreaker","LoadWordBreaker method [search]","LoadWordBreaker method [search]","ISearchLanguageSupport interface","_search_ISearchLanguageSupport_LoadWordBreaker","search._search_ISearchLanguageSupport_LoadWordBreaker","searchapi/ISearchLanguageSupport::LoadWordBreaker"]
old-location: search\_search_ISearchLanguageSupport_LoadWordBreaker.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\loadwordbreaker.htm
ms.date: 12/05/2018
ms.keywords: ISearchLanguageSupport interface [search],LoadWordBreaker method, ISearchLanguageSupport.LoadWordBreaker, ISearchLanguageSupport::LoadWordBreaker, LoadWordBreaker, LoadWordBreaker method [search], LoadWordBreaker method [search],ISearchLanguageSupport interface, _search_ISearchLanguageSupport_LoadWordBreaker, search._search_ISearchLanguageSupport_LoadWordBreaker, searchapi/ISearchLanguageSupport::LoadWordBreaker
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
 - ISearchLanguageSupport::LoadWordBreaker
 - searchapi/ISearchLanguageSupport::LoadWordBreaker
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
 - ISearchLanguageSupport.LoadWordBreaker
---

# ISearchLanguageSupport::LoadWordBreaker


## -description

Retrieves an interface to the word breaker registered for the specified language code identifier (LCID).

## -parameters

### -param lcid [in]

Type: <b>LCID</b>

The LCID requested.

### -param riid [in]

Type: <b>REFIID</b>

IID of the interface to be queried.

### -param ppWordBreaker [out]

Type: <b>void**</b>

On return, contains the address of a pointer to the interface of the LCID contained in <i>pLcidUsed</i>.

### -param pLcidUsed [out]

Type: <b>LCID*</b>

On return, contains a pointer to the actual LCID used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

