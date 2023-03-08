---
UID: NF:structuredquery.IQueryParserManager.CreateLoadedParser
title: IQueryParserManager::CreateLoadedParser (structuredquery.h)
description: Creates a new instance of a IQueryParser interface implementation. This instance of the query parser is loaded with the schema for the specified catalog and is localized to a specified language. All other settings are initialized to default settings.
helpviewer_keywords: ["CreateLoadedParser","CreateLoadedParser method [search]","CreateLoadedParser method [search]","IQueryParserManager interface","IQueryParserManager interface [search]","CreateLoadedParser method","IQueryParserManager.CreateLoadedParser","IQueryParserManager::CreateLoadedParser","_search_IQueryParserManager_CreateLoadedParser","search._search_IQueryParserManager_CreateLoadedParser","structuredquery/IQueryParserManager::CreateLoadedParser"]
old-location: search\_search_IQueryParserManager_CreateLoadedParser.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\createloadedparser.htm
ms.date: 12/05/2018
ms.keywords: CreateLoadedParser, CreateLoadedParser method [search], CreateLoadedParser method [search],IQueryParserManager interface, IQueryParserManager interface [search],CreateLoadedParser method, IQueryParserManager.CreateLoadedParser, IQueryParserManager::CreateLoadedParser, _search_IQueryParserManager_CreateLoadedParser, search._search_IQueryParserManager_CreateLoadedParser, structuredquery/IQueryParserManager::CreateLoadedParser
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IQueryParserManager::CreateLoadedParser
 - structuredquery/IQueryParserManager::CreateLoadedParser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQueryParserManager.CreateLoadedParser
---

# IQueryParserManager::CreateLoadedParser


## -description

Creates a new instance of a <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparser">IQueryParser</a> interface implementation. This instance of the query parser is loaded with the schema for the specified catalog and is localized to a specified language. All other settings are initialized to default settings.

## -parameters

### -param pszCatalog [in]

Type: <b>LPCWSTR</b>

The name of the catalog to use. Permitted values are <code>SystemIndex</code> and an empty string (for a trivial schema with no properties).

### -param langidForKeywords [in]

Type: <b>LANGID</b>

The <a href="/windows/desktop/Intl/language-identifiers">LANGID</a> used to select the localized language for keywords.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparser">IQueryParser</a> interface implementation.

### -param ppQueryParser [out, retval]

Type: <b>void**</b>

Receives a pointer to the newly created parser. The calling application must release it by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If %LOCALAPPDATA% is not available, then this method fails. You should call <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-setoption">IQueryParserManager::SetOption</a> to point to a different folder like %ProgramData%.