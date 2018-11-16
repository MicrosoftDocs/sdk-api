---
UID: NF:structuredquery.IConditionFactory2.CreateStringLeaf
title: IConditionFactory2::CreateStringLeaf
author: windows-sdk-content
description: Creates a leaf condition node for a string value that represents a comparison of property value and constant value. The returned object supports ICondition and ICondition2.
old-location: search\_search_IConditionFactory2_CreateStringLeaf.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\createstringleaf.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateStringLeaf, CreateStringLeaf method [search], CreateStringLeaf method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateStringLeaf method, IConditionFactory2.CreateStringLeaf, IConditionFactory2::CreateStringLeaf, _search_IConditionFactory2_CreateStringLeaf, search._search_IConditionFactory2_CreateStringLeaf, structuredquery/IConditionFactory2::CreateStringLeaf
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
 - IConditionFactory2.CreateStringLeaf
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
- IConditionFactory2.CreateStringLeaf
: 
---

# IConditionFactory2::CreateStringLeaf


## -description


Creates a leaf condition node for a string value that represents a comparison of property value and constant value. The returned object supports             <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The name of the property of the leaf condition as a REFPROPERTYKEY. If the leaf has no particular property, use PKEY_Null.


### -param cop [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a> enumeration. If the leaf has no particular operation, then use <i>COP_IMPLICIT</i>.


### -param pszValue [in]

Type: <b>LPCWSTR</b>

The value to be compared, or <b>NULL</b> for an unspecified property. The locale name of the leaf node is LOCALE_NAME_USER_DEFAULT.


### -param pszLocaleName [in]

Type: <b>LPCWSTR</b>

The name of the locale of the lead condition, or <b>NULL</b> for a plain string. The locale name of the leaf node is LOCALE_NAME_USER_DEFAULT.


### -param cco [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a> enumeration.


### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="https://msdn.microsoft.com/en-us/library/ms683764(v=VS.85).aspx">IEnumUnknown</a>, IID_IEnumVARIANT, or (for a negation condition) IID_ICondition.


### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a> objects.


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
 

 

