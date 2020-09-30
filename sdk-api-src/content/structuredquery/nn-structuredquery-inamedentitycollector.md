---
UID: NN:structuredquery.INamedEntityCollector
title: INamedEntityCollector (structuredquery.h)
description: Provides a method to accumulate named entities as identified by an IConditionGenerator object.
helpviewer_keywords: ["INamedEntityCollector","INamedEntityCollector interface [search]","INamedEntityCollector interface [search]","described","_search_INamedEntityCollector","search._search_INamedEntityCollector","structuredquery/INamedEntityCollector"]
old-location: search\_search_INamedEntityCollector.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\inamedentitycollector\inamedentitycollector.htm
ms.date: 12/05/2018
ms.keywords: INamedEntityCollector, INamedEntityCollector interface [search], INamedEntityCollector interface [search],described, _search_INamedEntityCollector, search._search_INamedEntityCollector, structuredquery/INamedEntityCollector
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
 - INamedEntityCollector
 - structuredquery/INamedEntityCollector
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
 - INamedEntityCollector
---

# INamedEntityCollector interface


## -description

Provides a method to accumulate named entities as identified by an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a> object. When a query parser parses an input string into condition nodes, the parser invokes an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a> object that, in turn, invokes this interface to collect possible named entities in the input string.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamedEntityCollector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INamedEntityCollector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamedEntityCollector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/structuredquery/nf-structuredquery-inamedentitycollector-add">Add</a>
</td>
<td align="left" width="63%">
Adds a single (potential) named entity to this <b>INamedEntityCollector</b> collection, as identified in a tokenized span of the input string being parsed.
        

</td>
</tr>
</table>