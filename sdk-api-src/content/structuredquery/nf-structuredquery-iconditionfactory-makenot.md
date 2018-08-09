---
UID: NF:structuredquery.IConditionFactory.MakeNot
title: IConditionFactory::MakeNot
author: windows-sdk-content
description: Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
old-location: search\_search_IConditionFactory_MakeNot.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\makenot.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IConditionFactory interface [search],MakeNot method, IConditionFactory.MakeNot, IConditionFactory::MakeNot, MakeNot, MakeNot method [search], MakeNot method [search],IConditionFactory interface, _search_IConditionFactory_MakeNot, search._search_IConditionFactory_MakeNot, structuredquery/IConditionFactory::MakeNot
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IConditionFactory.MakeNot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionFactory::MakeNot


## -description


Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        


## -parameters




### -param pcSub [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> subnode to be negated.
            


### -param fSimplify [in]

Type: <b>BOOL</b>

<b>TRUE</b> to logically simplify the result if possible; <b>FALSE</b> otherwise. In a query builder scenario, <i>fSimplify</i> should typically be set to VARIANT_FALSE.
            


### -param ppcResult [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>**</b>

Receives a pointer to the new <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> node.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Logically simplifying a condition node usually results in a smaller, more easily traversed and processed condition tree. For example, if <i>pcSub</i> is itself a negation condition with a subcondition C, then the double negation is logically resolved, and <i>ppcResult</i> is set to C. Without simplification, the resulting tree would look like NOT — NOT — C.
                

Applications that need to execute queries based on the condition tree would typically benefit from setting this parameter to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742799(v=VS.85).aspx">IConditionFactory2</a>



<b>Reference</b>
 

 

