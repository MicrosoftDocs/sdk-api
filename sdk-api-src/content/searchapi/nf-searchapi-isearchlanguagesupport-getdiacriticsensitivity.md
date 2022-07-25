---
UID: NF:searchapi.ISearchLanguageSupport.GetDiacriticSensitivity
title: ISearchLanguageSupport::GetDiacriticSensitivity (searchapi.h)
description: Gets the sensitivity of an implemented ISearchLanguageSupport interface to diacritics. A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.
helpviewer_keywords: ["GetDiacriticSensitivity","GetDiacriticSensitivity method [search]","GetDiacriticSensitivity method [search]","ISearchLanguageSupport interface","ISearchLanguageSupport interface [search]","GetDiacriticSensitivity method","ISearchLanguageSupport.GetDiacriticSensitivity","ISearchLanguageSupport::GetDiacriticSensitivity","_search_ISearchLanguageSupport_GetDiacriticSensitivity","search._search_ISearchLanguageSupport_GetDiacriticSensitivity","searchapi/ISearchLanguageSupport::GetDiacriticSensitivity"]
old-location: search\_search_ISearchLanguageSupport_GetDiacriticSensitivity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\getdiacriticsensitivity.htm
ms.date: 12/05/2018
ms.keywords: GetDiacriticSensitivity, GetDiacriticSensitivity method [search], GetDiacriticSensitivity method [search],ISearchLanguageSupport interface, ISearchLanguageSupport interface [search],GetDiacriticSensitivity method, ISearchLanguageSupport.GetDiacriticSensitivity, ISearchLanguageSupport::GetDiacriticSensitivity, _search_ISearchLanguageSupport_GetDiacriticSensitivity, search._search_ISearchLanguageSupport_GetDiacriticSensitivity, searchapi/ISearchLanguageSupport::GetDiacriticSensitivity
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
 - ISearchLanguageSupport::GetDiacriticSensitivity
 - searchapi/ISearchLanguageSupport::GetDiacriticSensitivity
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
 - ISearchLanguageSupport.GetDiacriticSensitivity
---

# ISearchLanguageSupport::GetDiacriticSensitivity


## -description

Gets the sensitivity of an implemented <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchlanguagesupport">ISearchLanguageSupport</a> interface to diacritics.  A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.

## -parameters

### -param pfDiacriticSensitive [out, retval]

Type: <b>BOOL*</b>

On return, contains a pointer to the sensitivity setting. <b>FALSE</b> indicates that the interface ignores diacritics; <b>TRUE</b> indicates the interface recognizes diacritics.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.