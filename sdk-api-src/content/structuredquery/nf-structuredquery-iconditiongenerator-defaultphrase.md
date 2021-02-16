---
UID: NF:structuredquery.IConditionGenerator.DefaultPhrase
title: IConditionGenerator::DefaultPhrase (structuredquery.h)
description: This method attempts to produce a phrase that, when recognized by this instance of IConditionGenerator, represents the type and value pair for an entity, relationship, or named entity.
helpviewer_keywords: ["DefaultPhrase","DefaultPhrase method [search]","DefaultPhrase method [search]","IConditionGenerator interface","IConditionGenerator interface [search]","DefaultPhrase method","IConditionGenerator.DefaultPhrase","IConditionGenerator::DefaultPhrase","_search_IConditionGenerator_DefaultPhrase","search._search_IConditionGenerator_DefaultPhrase","structuredquery/IConditionGenerator::DefaultPhrase"]
old-location: search\_search_IConditionGenerator_DefaultPhrase.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\defaultphrase.htm
ms.date: 12/05/2018
ms.keywords: DefaultPhrase, DefaultPhrase method [search], DefaultPhrase method [search],IConditionGenerator interface, IConditionGenerator interface [search],DefaultPhrase method, IConditionGenerator.DefaultPhrase, IConditionGenerator::DefaultPhrase, _search_IConditionGenerator_DefaultPhrase, search._search_IConditionGenerator_DefaultPhrase, structuredquery/IConditionGenerator::DefaultPhrase
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
 - IConditionGenerator::DefaultPhrase
 - structuredquery/IConditionGenerator::DefaultPhrase
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
 - IConditionGenerator.DefaultPhrase
---

# IConditionGenerator::DefaultPhrase


## -description

This method attempts to produce a phrase that, when recognized by this instance of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a>, represents the type and value pair for an entity, relationship, or named entity.

## -parameters

### -param pszValueType [in]

Type: <b>LPCWSTR</b>

The semantic type of the value in <i>ppropvar</i>.

### -param ppropvar [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT const</a>*</b>

The value to be processed.

### -param fUseEnglish [in]

Type: <b>BOOL</b>

 The parameter fUseEnglish is reserved: it should be ignored by implementors, and callers should pass <b>FALSE</b>.

### -param ppszPhrase [out, retval, optional]

Type: <b>LPWSTR*</b>

Receives a pointer to the phrase representing the value. If no phrase can be produced, this parameter is set to <b>NULL</b> and the method returns S_FALSE.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if the input arguments are valid but no phrase can be produced, and an error value otherwise.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a>



<b>Reference</b>