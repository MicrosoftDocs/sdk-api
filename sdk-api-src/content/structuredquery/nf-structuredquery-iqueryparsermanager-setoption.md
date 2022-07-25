---
UID: NF:structuredquery.IQueryParserManager.SetOption
title: IQueryParserManager::SetOption (structuredquery.h)
description: Changes a single option in this IQueryParserManager object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.
helpviewer_keywords: ["IQueryParserManager interface [search]","SetOption method","IQueryParserManager.SetOption","IQueryParserManager::SetOption","SetOption","SetOption method [search]","SetOption method [search]","IQueryParserManager interface","_search_IQueryParserManager_SetOption","search._search_IQueryParserManager_SetOption","structuredquery/IQueryParserManager::SetOption"]
old-location: search\_search_IQueryParserManager_SetOption.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\setoption.htm
ms.date: 12/05/2018
ms.keywords: IQueryParserManager interface [search],SetOption method, IQueryParserManager.SetOption, IQueryParserManager::SetOption, SetOption, SetOption method [search], SetOption method [search],IQueryParserManager interface, _search_IQueryParserManager_SetOption, search._search_IQueryParserManager_SetOption, structuredquery/IQueryParserManager::SetOption
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
 - IQueryParserManager::SetOption
 - structuredquery/IQueryParserManager::SetOption
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
 - IQueryParserManager.SetOption
---

# IQueryParserManager::SetOption


## -description

Changes a single option in this <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparsermanager">IQueryParserManager</a> object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.

## -parameters

### -param option [in]

Type: <b><a href="/windows/win32/api/structuredquery/ne-structuredquery-query_parser_manager_option">QUERY_PARSER_MANAGER_OPTION</a></b>

The <a href="/windows/win32/api/structuredquery/ne-structuredquery-query_parser_manager_option">QUERY_PARSER_MANAGER_OPTION</a> to be changed.

### -param pOptionValue [in]

Type: <b>PROPVARIANT const*</b>

A pointer to the value to use for the option selected.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.