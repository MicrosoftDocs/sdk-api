---
UID: NF:structuredquery.IQueryParserManager.InitializeOptions
title: IQueryParserManager::InitializeOptions
author: windows-sdk-content
description: Sets the flags for Natural Query Syntax (NQS) and automatic wildcard characters for the specified query parser.
old-location: search\_search_IQueryParserManager_InitializeOptions.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\initializeoptions.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IQueryParserManager interface [search],InitializeOptions method, IQueryParserManager.InitializeOptions, IQueryParserManager::InitializeOptions, InitializeOptions, InitializeOptions method [search], InitializeOptions method [search],IQueryParserManager interface, _search_IQueryParserManager_InitializeOptions, search._search_IQueryParserManager_InitializeOptions, structuredquery/IQueryParserManager::InitializeOptions
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQueryParserManager.InitializeOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IQueryParserManager::InitializeOptions


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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231353(v=VS.85).aspx">IQueryParser</a>*</b>

Pointer to the query parser object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



