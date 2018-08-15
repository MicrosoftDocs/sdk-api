---
UID: NF:searchapi.ISearchLanguageSupport.LoadStemmer
title: ISearchLanguageSupport::LoadStemmer
author: windows-sdk-content
description: Retrieves an interface to the word stemmer registered for the specified language code identifier (LCID).
old-location: search\_search_ISearchLanguageSupport_LoadStemmer.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\isearchlanguagesupport\loadstemmer.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchLanguageSupport interface [search],LoadStemmer method, ISearchLanguageSupport.LoadStemmer, ISearchLanguageSupport::LoadStemmer, LoadStemmer, LoadStemmer method [search], LoadStemmer method [search],ISearchLanguageSupport interface, _search_ISearchLanguageSupport_LoadStemmer, search._search_ISearchLanguageSupport_LoadStemmer, searchapi/ISearchLanguageSupport::LoadStemmer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchLanguageSupport.LoadStemmer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchLanguageSupport::LoadStemmer


## -description


Retrieves an interface to the word stemmer registered for the specified language code identifier (LCID).


## -parameters




### -param lcid [in]

Type: <b>LCID</b>

The LCID requested.


### -param riid [in]

Type: <b>REFIID</b>

IID of the interface to be queried.


### -param ppStemmer [out]

Type: <b>void**</b>

On return, contains the address of a pointer to the interface of the LCID contained in <i>pLcidUsed</i>.


### -param pLcidUsed [out]

Type: <b>LCID*</b>

On return, contains a pointer to the actual LCID used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



