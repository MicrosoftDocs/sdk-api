---
UID: NF:structuredquery.IConditionFactory2.ResolveCondition
title: IConditionFactory2::ResolveCondition
author: windows-sdk-content
description: Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports ICondition and ICondition2.
old-location: search\_search_IConditionFactory2_ResolveCondition.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\resolvecondition.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IConditionFactory2 interface [search],ResolveCondition method, IConditionFactory2.ResolveCondition, IConditionFactory2::ResolveCondition, ResolveCondition, ResolveCondition method [search], ResolveCondition method [search],IConditionFactory2 interface, _search_IConditionFactory2_ResolveCondition, search._search_IConditionFactory2_ResolveCondition, structuredquery/IConditionFactory2::ResolveCondition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IConditionFactory2.ResolveCondition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionFactory2::ResolveCondition


## -description


Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.


## -parameters




### -param pc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> object to be resolved.


### -param sqro [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd797951(v=VS.85).aspx">STRUCTURED_QUERY_RESOLVE_OPTION</a></b>

Specifies zero or more of the <a href="https://msdn.microsoft.com/en-us/library/Dd797951(v=VS.85).aspx">STRUCTURED_QUERY_RESOLVE_OPTION</a> flags. The <i>SQRO_NULL_VALUE_TYPE_FOR_PLAIN_VALUES</i> flag is automatically added to <i>sqro</i>.


### -param pstReferenceTime [in, optional]

Type: <b>SYSTEMTIME const*</b>

Pointer to a <b>SYSTEMTIME</b> value to use as the reference date and time. A null pointer can be passed if <i>sqro</i> is set to the <i>SQRO_DONT_RESOLVE_DATETIME</i> flag.


### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the  enumerating interface: either <a href="https://msdn.microsoft.com/en-us/library/ms683764(v=VS.85).aspx">IEnumUnknown</a>, <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a>, or (for a negation condition) IID_ICondition.


### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a> objects.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting 
condition trees.

Refer to the <a href="https://msdn.microsoft.com/en-us/library/Bb231387(v=VS.85).aspx">Resolve</a> method for additional detail.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742799(v=VS.85).aspx">IConditionFactory2</a>



<b>Reference</b>
 

 

