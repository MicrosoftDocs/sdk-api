---
UID: NF:structuredquery.IConditionFactory2.CreateTrueFalse
title: IConditionFactory2::CreateTrueFalse
author: windows-sdk-content
description: Creates a search condition that is either TRUE or FALSE.
old-location: search\_search_IConditionFactory2_CreateTrueFalse.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\createtruefalse.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateTrueFalse, CreateTrueFalse method [search], CreateTrueFalse method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateTrueFalse method, IConditionFactory2.CreateTrueFalse, IConditionFactory2::CreateTrueFalse, _search_IConditionFactory2_CreateTrueFalse, search._search_IConditionFactory2_CreateTrueFalse, structuredquery/IConditionFactory2::CreateTrueFalse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IConditionFactory2.CreateTrueFalse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- structuredquery.h
: 
- IConditionFactory2.CreateTrueFalse
: 
---

# IConditionFactory2::CreateTrueFalse


## -description


Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



## -parameters




### -param fVal

TBD


### -param cco [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a> enumeration.


### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="https://msdn.microsoft.com/en-us/library/ms683764(v=VS.85).aspx">IEnumUnknown</a>, <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a>, or (for a negation condition) IID_ICondition.


### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a> objects.


#### - fValue [in]

Type: <b>BOOL</b>

The value of the search condition to use. <i>fValue</i> should typically be set to VARIANT_FALSE.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For default options, use the <i>CONDITION_CREATION_DEFAULT</i> flag.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742799(v=VS.85).aspx">IConditionFactory2</a>



<b>Reference</b>
 

 

