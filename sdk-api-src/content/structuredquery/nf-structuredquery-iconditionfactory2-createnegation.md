---
UID: NF:structuredquery.IConditionFactory2.CreateNegation
title: IConditionFactory2::CreateNegation (structuredquery.h)
author: windows-sdk-content
description: Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
old-location: search\_search_IConditionFactory2_CreateNegation.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\createnegation.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateNegation, CreateNegation method [search], CreateNegation method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateNegation method, IConditionFactory2.CreateNegation, IConditionFactory2::CreateNegation, _search_IConditionFactory2_CreateNegation, search._search_IConditionFactory2_CreateNegation, structuredquery/IConditionFactory2::CreateNegation
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
 - IConditionFactory2.CreateNegation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConditionFactory2::CreateNegation


## -description


Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        


## -parameters




### -param pcSub [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> subnode to be negated. For default options, use the <i>CONDITION_CREATION_DEFAULT</i> flag.
            


### -param cco [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a> enumeration.


### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="https://msdn.microsoft.com/en-us/library/ms683764(v=VS.85).aspx">IEnumUnknown</a>, <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a>, or (for a negation condition) IID_ICondition.


### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a> objects.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



  Logically simplifying a condition node usually results in a smaller, more easily traversed and processed condition tree. For example, if <i>pcSub</i> is itself a negation condition with a subcondition C, then the double negation is logically resolved, and <i>ppcResult</i> is set to C. Without simplification, the resulting tree would look like NOT — NOT — C.

Applications that need to execute queries based on the condition tree would typically benefit from setting this parameter to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742799(v=VS.85).aspx">IConditionFactory2</a>



<b>Reference</b>
 

 

