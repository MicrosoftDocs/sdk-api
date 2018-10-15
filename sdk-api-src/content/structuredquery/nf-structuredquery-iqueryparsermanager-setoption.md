---
UID: NF:structuredquery.IQueryParserManager.SetOption
title: IQueryParserManager::SetOption
author: windows-sdk-content
description: Changes a single option in this IQueryParserManager object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.
old-location: search\_search_IQueryParserManager_SetOption.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\setoption.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IQueryParserManager interface [search],SetOption method, IQueryParserManager.SetOption, IQueryParserManager::SetOption, SetOption, SetOption method [search], SetOption method [search],IQueryParserManager interface, _search_IQueryParserManager_SetOption, search._search_IQueryParserManager_SetOption, structuredquery/IQueryParserManager::SetOption
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
 - IQueryParserManager.SetOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IQueryParserManager::SetOption


## -description


Changes a single option in this <a href="https://msdn.microsoft.com/en-us/library/Bb231349(v=VS.85).aspx">IQueryParserManager</a> object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.


## -parameters




### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965700(v=VS.85).aspx">QUERY_PARSER_MANAGER_OPTION</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Aa965700(v=VS.85).aspx">QUERY_PARSER_MANAGER_OPTION</a> to be changed.


### -param pOptionValue [in]

Type: <b>PROPVARIANT const*</b>

A pointer to the value to use for the option selected.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



