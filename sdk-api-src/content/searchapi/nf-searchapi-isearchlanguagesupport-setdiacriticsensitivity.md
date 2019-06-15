---
UID: NF:searchapi.ISearchLanguageSupport.SetDiacriticSensitivity
title: ISearchLanguageSupport::SetDiacriticSensitivity (searchapi.h)
author: windows-sdk-content
description: Sets a value that indicates whether an implemented ISearchLanguageSupport interface is sensitive to diacritics. A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.
old-location: search\_search_ISearchLanguageSupport_SetDiacriticSensitivity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\setdiacriticsensitivity.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchLanguageSupport interface [search],SetDiacriticSensitivity method, ISearchLanguageSupport.SetDiacriticSensitivity, ISearchLanguageSupport::SetDiacriticSensitivity, SetDiacriticSensitivity, SetDiacriticSensitivity method [search], SetDiacriticSensitivity method [search],ISearchLanguageSupport interface, _search_ISearchLanguageSupport_SetDiacriticSensitivity, search._search_ISearchLanguageSupport_SetDiacriticSensitivity, searchapi/ISearchLanguageSupport::SetDiacriticSensitivity
ms.topic: method
f1_keywords: ["searchapi/ISearchLanguageSupport.SetDiacriticSensitivity"]
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
 - ISearchLanguageSupport.SetDiacriticSensitivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchLanguageSupport::SetDiacriticSensitivity


## -description


Sets a value that indicates whether an implemented <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchlanguagesupport">ISearchLanguageSupport</a> interface is sensitive to diacritics. A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation. 


## -parameters




### -param fDiacriticSensitive [in]

Type: <b>BOOL</b>

A Boolean value that indicates whether the interface is sensitive to diacritics. The default setting is <b>FALSE</b>, indicating that the interface ignores diacritical characters.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



