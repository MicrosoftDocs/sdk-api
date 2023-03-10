---
UID: NN:structuredquery.IConditionFactory
title: IConditionFactory (structuredquery.h)
description: Provides methods for creating or resolving a condition tree that was obtained by parsing a query string.
helpviewer_keywords: ["IConditionFactory","IConditionFactory interface [search]","IConditionFactory interface [search]","described","_search_IConditionFactory","search._search_IConditionFactory","structuredquery/IConditionFactory"]
old-location: search\_search_IConditionFactory.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\iconditionfactory.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory, IConditionFactory interface [search], IConditionFactory interface [search],described, _search_IConditionFactory, search._search_IConditionFactory, structuredquery/IConditionFactory
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
 - IConditionFactory
 - structuredquery/IConditionFactory
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
 - IConditionFactory
---

# IConditionFactory interface


## -description

Provides methods for creating or resolving a condition tree that was obtained by parsing a query string.

## -inheritance

The <b>IConditionFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConditionFactory</b> also has these types of members:

## -remarks

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>
