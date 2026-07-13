---
UID: NE:structuredquerycondition.tagCONDITION_OPERATION
title: CONDITION_OPERATION (structuredquerycondition.h)
description: Provides a set of flags to be used with following methods to indicate the operation in ICondition::GetComparisonInfo, ICondition2::GetLeafConditionInfo, IConditionFactory::MakeLeaf, IConditionFactory2::CreateBooleanLeaf, IConditionFactory2::CreateIntegerLeaf, IConditionFactory2::MakeLeaf, IConditionFactory2::CreateStringLeaf, and IConditionGenerator::GenerateForLeaf.
helpviewer_keywords: ["CONDITION_OPERATION","CONDITION_OPERATION enumeration [search]","COP_APPLICATION_SPECIFIC","COP_DOSWILDCARDS","COP_EQUAL","COP_GREATERTHAN","COP_GREATERTHANOREQUAL","COP_IMPLICIT","COP_LESSTHAN","COP_LESSTHANOREQUAL","COP_NOTEQUAL","COP_VALUE_CONTAINS","COP_VALUE_ENDSWITH","COP_VALUE_NOTCONTAINS","COP_VALUE_STARTSWITH","COP_WORD_EQUAL","COP_WORD_STARTSWITH","_search_CONDITION_OPERATION","search._search_CONDITION_OPERATION","structuredquerycondition/CONDITION_OPERATION","structuredquerycondition/COP_APPLICATION_SPECIFIC","structuredquerycondition/COP_DOSWILDCARDS","structuredquerycondition/COP_EQUAL","structuredquerycondition/COP_GREATERTHAN","structuredquerycondition/COP_GREATERTHANOREQUAL","structuredquerycondition/COP_IMPLICIT","structuredquerycondition/COP_LESSTHAN","structuredquerycondition/COP_LESSTHANOREQUAL","structuredquerycondition/COP_NOTEQUAL","structuredquerycondition/COP_VALUE_CONTAINS","structuredquerycondition/COP_VALUE_ENDSWITH","structuredquerycondition/COP_VALUE_NOTCONTAINS","structuredquerycondition/COP_VALUE_STARTSWITH","structuredquerycondition/COP_WORD_EQUAL","structuredquerycondition/COP_WORD_STARTSWITH"]
old-location: search\_search_CONDITION_OPERATION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\condition_operation.htm
ms.date: 12/05/2018
ms.keywords: CONDITION_OPERATION, CONDITION_OPERATION enumeration [search], COP_APPLICATION_SPECIFIC, COP_DOSWILDCARDS, COP_EQUAL, COP_GREATERTHAN, COP_GREATERTHANOREQUAL, COP_IMPLICIT, COP_LESSTHAN, COP_LESSTHANOREQUAL, COP_NOTEQUAL, COP_VALUE_CONTAINS, COP_VALUE_ENDSWITH, COP_VALUE_NOTCONTAINS, COP_VALUE_STARTSWITH, COP_WORD_EQUAL, COP_WORD_STARTSWITH, _search_CONDITION_OPERATION, search._search_CONDITION_OPERATION, structuredquerycondition/CONDITION_OPERATION, structuredquerycondition/COP_APPLICATION_SPECIFIC, structuredquerycondition/COP_DOSWILDCARDS, structuredquerycondition/COP_EQUAL, structuredquerycondition/COP_GREATERTHAN, structuredquerycondition/COP_GREATERTHANOREQUAL, structuredquerycondition/COP_IMPLICIT, structuredquerycondition/COP_LESSTHAN, structuredquerycondition/COP_LESSTHANOREQUAL, structuredquerycondition/COP_NOTEQUAL, structuredquerycondition/COP_VALUE_CONTAINS, structuredquerycondition/COP_VALUE_ENDSWITH, structuredquerycondition/COP_VALUE_NOTCONTAINS, structuredquerycondition/COP_VALUE_STARTSWITH, structuredquerycondition/COP_WORD_EQUAL, structuredquerycondition/COP_WORD_STARTSWITH
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CONDITION_OPERATION
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - tagCONDITION_OPERATION
 - structuredquerycondition/tagCONDITION_OPERATION
 - CONDITION_OPERATION
 - structuredquerycondition/CONDITION_OPERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquerycondition.h
api_name:
 - CONDITION_OPERATION
---

# CONDITION_OPERATION enumeration


## -description

Provides a set of flags to be used with following methods to indicate the operation in 
    <a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo">ICondition::GetComparisonInfo</a>, 
    <a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition2-getleafconditioninfo">ICondition2::GetLeafConditionInfo</a>, 
    <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-makeleaf">IConditionFactory::MakeLeaf</a>, 
    <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createbooleanleaf">IConditionFactory2::CreateBooleanLeaf</a>, 
    <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createintegerleaf">IConditionFactory2::CreateIntegerLeaf</a>, 
    <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createleaf">IConditionFactory2::MakeLeaf</a>, 
    <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createstringleaf">IConditionFactory2::CreateStringLeaf</a>, and 
    <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">IConditionGenerator::GenerateForLeaf</a>.

## -enum-fields

### -field COP_IMPLICIT:0

An implicit comparison between the value of the property and the value of the constant. For an unresolved condition, <a href="/windows/desktop/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">COP_IMPLICIT</a> means that a user did not type an operation. In contrast, a resolved condition will always have a condition other than the <b>COP_IMPLICIT</b> operation.

### -field COP_EQUAL

The value of the property and the value of the constant must be equal.

### -field COP_NOTEQUAL

The value of the property and the value of the constant must not be equal.

### -field COP_LESSTHAN

The value of the property must be less than the value of the constant.

### -field COP_GREATERTHAN

The value of the property must be greater than the value of the constant.

### -field COP_LESSTHANOREQUAL

The value of the property must be less than or equal to the value of the constant.

### -field COP_GREATERTHANOREQUAL

The value of the property must be greater than or equal to the value of the constant.

### -field COP_VALUE_STARTSWITH

The value of the property must begin with the value of the constant.

### -field COP_VALUE_ENDSWITH

The value of the property must end with the value of the constant.

### -field COP_VALUE_CONTAINS

The value of the property must contain the value of the constant.

### -field COP_VALUE_NOTCONTAINS

The value of the property must not contain the value of the constant.

### -field COP_DOSWILDCARDS

The value of the property must match the value of the constant, where '?' matches any single character and '*' matches any sequence of characters.

### -field COP_WORD_EQUAL

The value of the property must contain a word that is the value of the constant.

### -field COP_WORD_STARTSWITH

The value of the property must contain a word that begins with the value of the constant.

### -field COP_APPLICATION_SPECIFIC

The application is free to interpret this in any suitable way.

## -remarks

Because a resolved condition never has a <b>COP_IMPLICIT</b> operation, applications that evaluate condition trees should not encounter it. However, <b>COP_IMPLICIT</b> could be used in comparing the output of either <a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo">ICondition::GetComparisonInfo</a> or <a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition2-getleafconditioninfo">ICondition2::GetLeafConditionInfo</a> for a parsed unresolved condition to the output for a resolved condition.

In Windows 7, this enumeration is defined in structuredquerycondition.idl and structuredquerycondition.h. Prior to Windows 7 this enumeration was declared in structuredquery.h and structuredquery.idl.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a>



<b>Reference</b>
