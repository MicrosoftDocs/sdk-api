---
UID: NN:structuredquerycondition.ICondition
title: ICondition (structuredquerycondition.h)
description: Provides methods for retrieving information about a search condition.
helpviewer_keywords: ["ICondition","ICondition interface [search]","ICondition interface [search]","described","_search_ICondition","search._search_ICondition","structuredquerycondition/ICondition"]
old-location: search\_search_ICondition.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\icondition.htm
ms.date: 12/05/2018
ms.keywords: ICondition, ICondition interface [search], ICondition interface [search],described, _search_ICondition, search._search_ICondition, structuredquerycondition/ICondition
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquerycondition.idl
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
 - ICondition
 - structuredquerycondition/ICondition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - ICondition
---

# ICondition interface


## -description

Provides methods for retrieving information about a search condition. An <b>ICondition</b> object represents the result of parsing an input string (using methods such as <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-parse">IQueryParser::Parse</a> or <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-getquery">IQuerySolution::GetQuery</a>) into a tree of search condition nodes. A node can be a logical AND, OR, or NOT for comparing subnodes, or it can be a leaf node comparing a property and a constant value.

## -inheritance

The <b>ICondition</b> interface inherits from <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>. <b>ICondition</b> also has these types of members:

## -remarks

Prior to Windows 7, this interface was only declared in structuredquery.h and structuredquery.idl. In Windows 7, this interface is also defined in structuredquerycondition.idl and structuredquerycondition.h.

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>



<b>Reference</b>
