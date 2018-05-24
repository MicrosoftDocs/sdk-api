---
UID: NF:searchapi.ISearchLanguageSupport.GetDiacriticSensitivity
title: ISearchLanguageSupport::GetDiacriticSensitivity
author: windows-driver-content
description: Gets the sensitivity of an implemented ISearchLanguageSupport interface to diacritics. A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.
old-location: search\_search_ISearchLanguageSupport_GetDiacriticSensitivity.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\getdiacriticsensitivity.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetDiacriticSensitivity, GetDiacriticSensitivity method [search], GetDiacriticSensitivity method [search],ISearchLanguageSupport interface, ISearchLanguageSupport interface [search],GetDiacriticSensitivity method, ISearchLanguageSupport.GetDiacriticSensitivity, ISearchLanguageSupport::GetDiacriticSensitivity, _search_ISearchLanguageSupport_GetDiacriticSensitivity, search._search_ISearchLanguageSupport_GetDiacriticSensitivity, searchapi/ISearchLanguageSupport::GetDiacriticSensitivity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	ISearchLanguageSupport.GetDiacriticSensitivity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchLanguageSupport::GetDiacriticSensitivity


## -description


Gets the sensitivity of an implemented <a href="https://msdn.microsoft.com/a1d1f2e2-c11d-4774-b15f-5a67ce9d5340">ISearchLanguageSupport</a> interface to diacritics.  A diacritic is an accent mark added to a letter to indicate a special phonetic value or pronunciation.


## -parameters




### -param pfDiacriticSensitive [out, retval]

Type: <b>BOOL*</b>

On return, contains a pointer to the sensitivity setting. <b>FALSE</b> indicates that the interface ignores diacritics; <b>TRUE</b> indicates the interface recognizes diacritics.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



