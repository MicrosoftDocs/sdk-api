---
UID: NE:structuredquerycondition.tagCONDITION_TYPE
title: CONDITION_TYPE (structuredquerycondition.h)
description: Provides a set of flags to be used with the following methods to indicate the type of condition tree node:\_ICondition::GetConditionType, IConditionFactory::MakeAndOr, IConditionFactory2::CreateCompoundFromArray, and IConditionFactory2::CreateCompoundFromObjectArray.
helpviewer_keywords: ["CONDITION_TYPE","CONDITION_TYPE enumeration [search]","CT_AND_CONDITION","CT_LEAF_CONDITION","CT_NOT_CONDITION","CT_OR_CONDITION","_search_CONDITION_TYPE","search._search_CONDITION_TYPE","structuredquerycondition/CONDITION_TYPE","structuredquerycondition/CT_AND_CONDITION","structuredquerycondition/CT_LEAF_CONDITION","structuredquerycondition/CT_NOT_CONDITION","structuredquerycondition/CT_OR_CONDITION"]
old-location: search\_search_CONDITION_TYPE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\condition_type.htm
ms.date: 12/05/2018
ms.keywords: CONDITION_TYPE, CONDITION_TYPE enumeration [search], CT_AND_CONDITION, CT_LEAF_CONDITION, CT_NOT_CONDITION, CT_OR_CONDITION, _search_CONDITION_TYPE, search._search_CONDITION_TYPE, structuredquerycondition/CONDITION_TYPE, structuredquerycondition/CT_AND_CONDITION, structuredquerycondition/CT_LEAF_CONDITION, structuredquerycondition/CT_NOT_CONDITION, structuredquerycondition/CT_OR_CONDITION
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
req.typenames: CONDITION_TYPE
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - tagCONDITION_TYPE
 - structuredquerycondition/tagCONDITION_TYPE
 - CONDITION_TYPE
 - structuredquerycondition/CONDITION_TYPE
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
 - CONDITION_TYPE
---

# CONDITION_TYPE enumeration


## -description

Provides a set of flags to be used with the following methods to indicate the type of condition tree node: 
        <a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getconditiontype">ICondition::GetConditionType</a>, 
        <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-makeandor">IConditionFactory::MakeAndOr</a>, 
        <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createcompoundfromarray">IConditionFactory2::CreateCompoundFromArray</a>, and 
        <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createcompoundfromobjectarray">IConditionFactory2::CreateCompoundFromObjectArray</a>.

## -enum-fields

### -field CT_AND_CONDITION:0

Indicates that the values of the subterms are combined by "AND".

### -field CT_OR_CONDITION

Indicates that the values of the subterms are combined by "OR".

### -field CT_NOT_CONDITION

Indicates a "NOT" comparison of subterms.

### -field CT_LEAF_CONDITION

Indicates that the node is a comparison between a property and a constant value using a <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>.

## -remarks

In Windows 7, this enumeration is defined in structuredquerycondition.idl and structuredquerycondition.h. Prior to Windows 7 this enumeration was declared in structuredquery.h and structuredquery.idl.

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a>



<b>Reference</b>
