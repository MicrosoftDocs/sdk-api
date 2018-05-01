---
UID: NF:structuredquery.IQueryParserManager.InitializeOptions
title: IQueryParserManager::InitializeOptions method
author: windows-driver-content
description: Sets the flags for Natural Query Syntax (NQS) and automatic wildcard characters for the specified query parser.
old-location: search\_search_IQueryParserManager_InitializeOptions.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\initializeoptions.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IQueryParserManager, IQueryParserManager interface [search], InitializeOptions method, IQueryParserManager::InitializeOptions, InitializeOptions method [search], InitializeOptions method [search], IQueryParserManager interface, InitializeOptions,IQueryParserManager.InitializeOptions, _search_IQueryParserManager_InitializeOptions, search._search_IQueryParserManager_InitializeOptions, structuredquery/IQueryParserManager::InitializeOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IQueryParserManager.InitializeOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQueryParserManager::InitializeOptions method


## -description


Sets the flags for Natural Query Syntax (NQS) and automatic wildcard characters for the specified query parser. If the query parser was created for the <code>SystemIndex</code> catalog, this method also sets up standard condition generators to be used later by the query parser object for recognizing named entities.



## -parameters




### -param fUnderstandNQS [in]

Type: <b>BOOL</b>

<b>BOOL</b> flag that controls whether NQS is supported by this instance of the query parser.


### -param fAutoWildCard [in]

Type: <b>BOOL</b>

<b>BOOL</b> flag that controls whether a wildcard character (*) is to be assumed after each word in the query (unless followed by punctuation other than a parenthesis).


### -param pQueryParser [in]

Type: <b><a href="https://msdn.microsoft.com/f022464d-9db6-42c8-a3fb-12c31ec48756">IQueryParser</a>*</b>

Pointer to the query parser object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



