---
UID: NF:structuredquery.IQueryParserManager.SetOption
title: IQueryParserManager::SetOption
author: windows-sdk-content
description: Changes a single option in this IQueryParserManager object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.
old-location: search\_search_IQueryParserManager_SetOption.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\setoption.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IQueryParserManager interface [search],SetOption method, IQueryParserManager.SetOption, IQueryParserManager::SetOption, SetOption, SetOption method [search], SetOption method [search],IQueryParserManager interface, _search_IQueryParserManager_SetOption, search._search_IQueryParserManager_SetOption, structuredquery/IQueryParserManager::SetOption
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQueryParserManager.SetOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQueryParserManager::SetOption


## -description


Changes a single option in this <a href="https://msdn.microsoft.com/ff1941e1-03f0-4fdb-a34b-61da4055f569">IQueryParserManager</a> object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.


## -parameters




### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/ad19e452-f457-4cd6-9d41-c9a61d94a685">QUERY_PARSER_MANAGER_OPTION</a></b>

The <a href="https://msdn.microsoft.com/ad19e452-f457-4cd6-9d41-c9a61d94a685">QUERY_PARSER_MANAGER_OPTION</a> to be changed.


### -param pOptionValue [in]

Type: <b>PROPVARIANT const*</b>

A pointer to the value to use for the option selected.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



