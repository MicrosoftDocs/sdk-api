---
UID: NF:structuredquery.IConditionFactory.Resolve
title: IConditionFactory::Resolve
author: windows-sdk-content
description: Performs a variety of transformations on a condition tree, including the following:\_resolves conditions with relative date/time expressions to conditions with absolute date/time (as a VT_FILETIME); turns other recognized named entities into condition trees with actual values; simplifies condition trees; replaces virtual or compound properties with OR trees of other properties; removes condition trees resulting from queries with property keywords that had no condition applied.
old-location: search\_search_IConditionFactory_Resolve.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\resolve.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IConditionFactory interface [search],Resolve method, IConditionFactory.Resolve, IConditionFactory::Resolve, Resolve, Resolve method [search], Resolve method [search],IConditionFactory interface, _search_IConditionFactory_Resolve, search._search_IConditionFactory_Resolve, structuredquery/IConditionFactory::Resolve
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IConditionFactory.Resolve
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionFactory::Resolve


## -description


Performs a variety of transformations on a condition tree, including the following: resolves conditions with relative date/time expressions to conditions with absolute date/time (as a VT_FILETIME); turns other recognized named entities into condition trees with actual values; simplifies condition trees; replaces virtual or compound properties with OR trees of other properties; removes condition trees resulting from queries with property keywords that had no condition applied.


## -parameters




### -param pc [in]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> object to be resolved.


### -param sqro [in]

Type: <b><a href="https://msdn.microsoft.com/84a052ae-4d05-438f-ab90-e1a248239aca">STRUCTURED_QUERY_RESOLVE_OPTION</a></b>

Specifies zero or more of the <a href="https://msdn.microsoft.com/84a052ae-4d05-438f-ab90-e1a248239aca">STRUCTURED_QUERY_RESOLVE_OPTION</a> flags. For <b>Windows 7 and later</b>, the SQRO_ADD_VALUE_TYPE_FOR_PLAIN_VALUES flag is automatically added to <i>sqro</i>.


### -param pstReferenceTime [in]

Type: <b>SYSTEMTIME const*</b>

A pointer to a <b>SYSTEMTIME</b> value to use as the reference date and time. A null pointer can be passed if <i>sqro</i> is set to SQRO_DONT_RESOLVE_DATETIME.


### -param ppcResolved [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>**</b>

Receives a pointer to the new <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> in which all time fields have been resolved to have values of type VT_FILETIME. This new condition tree is the resolved version of <i>pc</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In a condition tree produced by the <a href="https://msdn.microsoft.com/2ca6ddfa-821c-4d84-abbf-61d25b633180">Parse</a> method and returned by <a href="https://msdn.microsoft.com/ef03828a-ac31-4e73-a8bb-44f0b1963107">GetQuery</a>, the leaves pair up properties with restrictions on these properties, and result in a condition tree that is partially finished. The <b>IConditionFactory::Resolve</b> method finishes such a condition tree by a process known as resolution. The input condition tree is not modified in any way. The output condition tree may share parts of the input condition that contained no leaf nodes with unresolved date/time values.

<div class="alert"><b>Note</b>  Resolving a leaf node often produces a non-leaf node.</div>
<div> </div>
For example, Structured Query supports relative date/time expressions, which remain unresolved until they are applied to some reference time. In a leaf node with semantic type <b>System.StructuredQueryType.DateTime</b>, the value can be either a VT_FILETIME or a VT_LPWSTR. VT_FILETIME is an absolute date/time so it is already resolved. VT_LPWSTR is a string representation of a relative date/time expression. The specified reference time should be a local time, but the resolved times in the resulting query expression will be in Coordinated Universal Time (UTC).

The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>



<b>Reference</b>
 

 

