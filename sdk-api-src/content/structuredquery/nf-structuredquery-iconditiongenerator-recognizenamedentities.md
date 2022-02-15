---
UID: NF:structuredquery.IConditionGenerator.RecognizeNamedEntities
title: IConditionGenerator::RecognizeNamedEntities (structuredquery.h)
description: Identifies named entities in an input string, and creates a collection containing them.
helpviewer_keywords: ["IConditionGenerator interface [search]","RecognizeNamedEntities method","IConditionGenerator.RecognizeNamedEntities","IConditionGenerator::RecognizeNamedEntities","RecognizeNamedEntities","RecognizeNamedEntities method [search]","RecognizeNamedEntities method [search]","IConditionGenerator interface","_search_IConditionGenerator_RecognizeNamedEntities","search._search_IConditionGenerator_RecognizeNamedEntities","structuredquery/IConditionGenerator::RecognizeNamedEntities"]
old-location: search\_search_IConditionGenerator_RecognizeNamedEntities.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\recognizenamedentities.htm
ms.date: 12/05/2018
ms.keywords: IConditionGenerator interface [search],RecognizeNamedEntities method, IConditionGenerator.RecognizeNamedEntities, IConditionGenerator::RecognizeNamedEntities, RecognizeNamedEntities, RecognizeNamedEntities method [search], RecognizeNamedEntities method [search],IConditionGenerator interface, _search_IConditionGenerator_RecognizeNamedEntities, search._search_IConditionGenerator_RecognizeNamedEntities, structuredquery/IConditionGenerator::RecognizeNamedEntities
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConditionGenerator::RecognizeNamedEntities
 - structuredquery/IConditionGenerator::RecognizeNamedEntities
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
 - IConditionGenerator.RecognizeNamedEntities
---

# IConditionGenerator::RecognizeNamedEntities


## -description

Identifies named entities in an input string, and creates a collection containing them. The value of each named entity is expressed as a string, which is then used by <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">IConditionGenerator::GenerateForLeaf</a>. The string can contain any data and be in any format, because it is not examined by any other components.

## -parameters

### -param pszInputString [in]

Type: <b>LPCWSTR</b>

The input string to be parsed.

### -param lcidUserLocale [in]

Type: <b>LCID</b>

The LCID against which named entities should be recognized.

### -param pTokenCollection [in]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-itokencollection">ITokenCollection</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-itokencollection">ITokenCollection</a> object that indicates how the input string was tokenized.

### -param pNamedEntities [in, out]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentitycollector">INamedEntityCollector</a>*</b>

On input, contains an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentitycollector">INamedEntityCollector</a> or <b>NULL</b>. On return, contains an <b>INamedEntityCollector</b> collection of the named entities.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Given an input string, a user locale (typically the user's default locale) and a tokenization of the input string, the <b>IConditionGenerator::RecognizeNamedEntities</b> method should be able to identify any named entities in that input string, and then add each entity to the named entity collection.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a>



<b>Reference</b>