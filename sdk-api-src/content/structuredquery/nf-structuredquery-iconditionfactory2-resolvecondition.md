---
UID: NF:structuredquery.IConditionFactory2.ResolveCondition
title: IConditionFactory2::ResolveCondition (structuredquery.h)
description: Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports ICondition and ICondition2.
helpviewer_keywords: ["IConditionFactory2 interface [search]","ResolveCondition method","IConditionFactory2.ResolveCondition","IConditionFactory2::ResolveCondition","ResolveCondition","ResolveCondition method [search]","ResolveCondition method [search]","IConditionFactory2 interface","_search_IConditionFactory2_ResolveCondition","search._search_IConditionFactory2_ResolveCondition","structuredquery/IConditionFactory2::ResolveCondition"]
old-location: search\_search_IConditionFactory2_ResolveCondition.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\resolvecondition.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory2 interface [search],ResolveCondition method, IConditionFactory2.ResolveCondition, IConditionFactory2::ResolveCondition, ResolveCondition, ResolveCondition method [search], ResolveCondition method [search],IConditionFactory2 interface, _search_IConditionFactory2_ResolveCondition, search._search_IConditionFactory2_ResolveCondition, structuredquery/IConditionFactory2::ResolveCondition
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IConditionFactory2::ResolveCondition
 - structuredquery/IConditionFactory2::ResolveCondition
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
 - IConditionFactory2.ResolveCondition
---

# IConditionFactory2::ResolveCondition


## -description

Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

## -parameters

### -param pc [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>*</b>

Pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> object to be resolved.

### -param sqro [in]

Type: <b><a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_resolve_option">STRUCTURED_QUERY_RESOLVE_OPTION</a></b>

Specifies zero or more of the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_resolve_option">STRUCTURED_QUERY_RESOLVE_OPTION</a> flags. The <i>SQRO_NULL_VALUE_TYPE_FOR_PLAIN_VALUES</i> flag is automatically added to <i>sqro</i>.

### -param pstReferenceTime [in, optional]

Type: <b>SYSTEMTIME const*</b>

Pointer to a <b>SYSTEMTIME</b> value to use as the reference date and time. A null pointer can be passed if <i>sqro</i> is set to the <i>SQRO_DONT_RESOLVE_DATETIME</i> flag.

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the  enumerating interface: either <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>, or (for a negation condition) IID_ICondition.

### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a> objects.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

Refer to the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-resolve">Resolve</a> method for additional detail.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>