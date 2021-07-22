---
UID: NF:structuredquery.INamedEntityCollector.Add
title: INamedEntityCollector::Add (structuredquery.h)
description: Adds a single (potential) named entity to this INamedEntityCollector collection, as identified in a tokenized span of the input string being parsed.
helpviewer_keywords: ["Add","Add method [search]","Add method [search]","INamedEntityCollector interface","INamedEntityCollector interface [search]","Add method","INamedEntityCollector.Add","INamedEntityCollector::Add","_search_INamedEntityCollector_Add","search._search_INamedEntityCollector_Add","structuredquery/INamedEntityCollector::Add"]
old-location: search\_search_INamedEntityCollector_Add.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\inamedentitycollector\add.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [search], Add method [search],INamedEntityCollector interface, INamedEntityCollector interface [search],Add method, INamedEntityCollector.Add, INamedEntityCollector::Add, _search_INamedEntityCollector_Add, search._search_INamedEntityCollector_Add, structuredquery/INamedEntityCollector::Add
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
 - INamedEntityCollector::Add
 - structuredquery/INamedEntityCollector::Add
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
 - INamedEntityCollector.Add
---

# INamedEntityCollector::Add


## -description

Adds a single (potential) named entity to this <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentitycollector">INamedEntityCollector</a> collection, as identified in a tokenized span of the input string being parsed.

## -parameters

### -param beginSpan [in]

Type: <b>ULONG</b>

The beginning of the overall token span, including any leading quotation marks.

### -param endSpan [in]

Type: <b>ULONG</b>

The end of the overall token span including any trailing quotation marks.

### -param beginActual [in]

Type: <b>ULONG</b>

The beginning of the part of the token span that identifies the potential named entity.

### -param endActual [in]

Type: <b>ULONG</b>

The end of the part of the token span that identifies the potential named entity.

### -param pType [in]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>*</b>

The semantic type of the named entity.

### -param pszValue [in]

Type: <b>LPCWSTR</b>

The name of the entity as a string.

### -param certainty [in]

Type: <b><a href="/windows/win32/api/structuredquery/ne-structuredquery-named_entity_certainty">NAMED_ENTITY_CERTAINTY</a></b>

One of the following values:
              

<table class="clsStd">
<tr>
<th>Value</th>
<th>Information</th>
</tr>
<tr>
<td>NEC_LOW</td>
<td>It could be this named entity, but additional evidence is advisable.</td>
</tr>
<tr>
<td>NEC_MEDIUM</td>
<td>It is likely this named entity; it is okay to use it.</td>
</tr>
<tr>
<td>NEC_HIGH</td>
<td>It almost certainly is this named entity; it should be okay to discard other possibilities.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a query parser parses an input string into condition nodes, the parser invokes an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a> object that, in turn, invokes <b>INamedEntityCollector::Add</b> to collect possible named entities in the input string. The <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a> object must call this method for each potential named entity it recognizes in the input string. For each entity, the condition generator must provide the following information: 

        

<ul>
<li>what part of the input string it covers</li>
<li>the semantic type of the named entity</li>
<li>a string representation of the value of the named entity</li>
<li>the level of certainty that the input really is that named entity</li>
</ul>
 
        If the named entity was used in the interpretation of the input string, the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">GenerateForLeaf</a> method of the condition generator will be invoked with the value string as one of the arguments.
          

The following relationship must be maintained between the four first arguments: <i>beginSpan</i>  = <i>beginActual</i> &lt; <i>endActual</i> = <i>endSpan</i>.