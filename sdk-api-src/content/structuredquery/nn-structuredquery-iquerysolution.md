---
UID: NN:structuredquery.IQuerySolution
title: IQuerySolution (structuredquery.h)
description: Provides methods that retrieve information about the interpretation of a parsed query.
helpviewer_keywords: ["IQuerySolution","IQuerySolution interface [search]","IQuerySolution interface [search]","described","_search_IQuerySolution","search._search_IQuerySolution","structuredquery/IQuerySolution"]
old-location: search\_search_IQuerySolution.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\iquerysolution.htm
ms.date: 12/05/2018
ms.keywords: IQuerySolution, IQuerySolution interface [search], IQuerySolution interface [search],described, _search_IQuerySolution, search._search_IQuerySolution, structuredquery/IQuerySolution
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
 - IQuerySolution
 - structuredquery/IQuerySolution
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
 - IQuerySolution
---

# IQuerySolution interface


## -description

Provides methods that retrieve information about the interpretation of a parsed query.

## -inheritance

The <b>IQuerySolution</b> interface inherits from <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>. <b>IQuerySolution</b> also has these types of members:

## -remarks

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.
