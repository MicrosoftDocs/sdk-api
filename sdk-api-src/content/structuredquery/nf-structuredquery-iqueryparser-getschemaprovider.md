---
UID: NF:structuredquery.IQueryParser.GetSchemaProvider
title: IQueryParser::GetSchemaProvider
author: windows-sdk-content
description: Retrieves a schema provider for browsing the currently loaded schema.
old-location: search\_search_IQueryParser_GetSchemaProvider.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\getschemaprovider.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetSchemaProvider, GetSchemaProvider method [search], GetSchemaProvider method [search],IQueryParser interface, IQueryParser interface [search],GetSchemaProvider method, IQueryParser.GetSchemaProvider, IQueryParser::GetSchemaProvider, _search_IQueryParser_GetSchemaProvider, search._search_IQueryParser_GetSchemaProvider, structuredquery/IQueryParser::GetSchemaProvider
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IQueryParser.GetSchemaProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQueryParser::GetSchemaProvider


## -description



          Retrieves a schema provider for browsing the currently loaded schema.
        


## -parameters




### -param ppSchemaProvider [out, retval]

Type: <b><a href="https://msdn.microsoft.com/c6cb1da0-5072-41b2-aa64-e39c8c97b2f8">ISchemaProvider</a>**</b>


              Receives the address of a pointer to an <a href="https://msdn.microsoft.com/c6cb1da0-5072-41b2-aa64-e39c8c97b2f8">ISchemaProvider</a> object. The calling application must release it by invoking its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



