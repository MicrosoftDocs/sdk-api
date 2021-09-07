---
UID: NF:structuredquery.IConditionFactory.Resolve
title: IConditionFactory::Resolve (structuredquery.h)
description: Performs a variety of transformations on a condition tree, including the following:\_resolves conditions with relative date/time expressions to conditions with absolute date/time (as a VT_FILETIME); turns other recognized named entities into condition trees with actual values; simplifies condition trees; replaces virtual or compound properties with OR trees of other properties; removes condition trees resulting from queries with property keywords that had no condition applied.
helpviewer_keywords: ["IConditionFactory interface [search]","Resolve method","IConditionFactory.Resolve","IConditionFactory::Resolve","Resolve","Resolve method [search]","Resolve method [search]","IConditionFactory interface","_search_IConditionFactory_Resolve","search._search_IConditionFactory_Resolve","structuredquery/IConditionFactory::Resolve"]
old-location: search\_search_IConditionFactory_Resolve.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\resolve.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory interface [search],Resolve method, IConditionFactory.Resolve, IConditionFactory::Resolve, Resolve, Resolve method [search], Resolve method [search],IConditionFactory interface, _search_IConditionFactory_Resolve, search._search_IConditionFactory_Resolve, structuredquery/IConditionFactory::Resolve
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
 - IConditionFactory::Resolve
 - structuredquery/IConditionFactory::Resolve
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
 - IConditionFactory.Resolve
---

# IConditionFactory::Resolve


## -description

Performs a variety of transformations on a condition tree, including the following: resolves conditions with relative date/time expressions to conditions with absolute date/time (as a VT_FILETIME); turns other recognized named entities into condition trees with actual values; simplifies condition trees; replaces virtual or compound properties with OR trees of other properties; removes condition trees resulting from queries with property keywords that had no condition applied.

## -parameters

### -param pc [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> object to be resolved.

### -param sqro [in]

Type: <b><a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_resolve_option">STRUCTURED_QUERY_RESOLVE_OPTION</a></b>

Specifies zero or more of the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_resolve_option">STRUCTURED_QUERY_RESOLVE_OPTION</a> flags. For <b>Windows 7 and later</b>, the SQRO_ADD_VALUE_TYPE_FOR_PLAIN_VALUES flag is automatically added to <i>sqro</i>.

### -param pstReferenceTime [in]

Type: <b>SYSTEMTIME const*</b>

A pointer to a <b>SYSTEMTIME</b> value to use as the reference date and time. A null pointer can be passed if <i>sqro</i> is set to SQRO_DONT_RESOLVE_DATETIME.

### -param ppcResolved [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Receives a pointer to the new <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> in which all time fields have been resolved to have values of type VT_FILETIME. This new condition tree is the resolved version of <i>pc</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In a condition tree produced by the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-parse">Parse</a> method and returned by <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-getquery">GetQuery</a>, the leaves pair up properties with restrictions on these properties, and result in a condition tree that is partially finished. The <b>IConditionFactory::Resolve</b> method finishes such a condition tree by a process known as resolution. The input condition tree is not modified in any way. The output condition tree may share parts of the input condition that contained no leaf nodes with unresolved date/time values.

<div class="alert"><b>Note</b>  Resolving a leaf node often produces a non-leaf node.</div>
<div> </div>
For example, Structured Query supports relative date/time expressions, which remain unresolved until they are applied to some reference time. In a leaf node with semantic type <b>System.StructuredQueryType.DateTime</b>, the value can be either a VT_FILETIME or a VT_LPWSTR. VT_FILETIME is an absolute date/time so it is already resolved. VT_LPWSTR is a string representation of a relative date/time expression. The specified reference time should be a local time, but the resolved times in the resulting query expression will be in Coordinated Universal Time (UTC).

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>