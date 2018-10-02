---
UID: NF:structuredquery.IConditionFactory.MakeAndOr
title: IConditionFactory::MakeAndOr
author: windows-sdk-content
description: Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions.
old-location: search\_search_IConditionFactory_MakeAndOr.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\makeandor.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IConditionFactory interface [search],MakeAndOr method, IConditionFactory.MakeAndOr, IConditionFactory::MakeAndOr, MakeAndOr, MakeAndOr method [search], MakeAndOr method [search],IConditionFactory interface, _search_IConditionFactory_MakeAndOr, search._search_IConditionFactory_MakeAndOr, structuredquery/IConditionFactory::MakeAndOr
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IConditionFactory.MakeAndOr
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IConditionFactory::MakeAndOr


## -description


Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions.


## -parameters




### -param ct [in]

Type: <b><a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a></b>

The <a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a> of the condition node. The <b>CONDITION_TYPE</b> must be either <b>CT_AND_CONDITION</b> or <b>CT_OR_CONDITION</b>.


### -param peuSubs [in]

Type: <b><a href="_com_IEnumUnknown">IEnumUnknown</a>*</b>

A pointer to an enumeration of <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> objects, or <b>NULL</b> for an empty enumeration.


### -param fSimplify [in]

Type: <b>BOOL</b>

<b>TRUE</b> to logically simplify the result, if possible; then the result will not necessarily to be of the specified kind. <b>FALSE</b> if the result should have exactly the prescribed structure. 


An application that plans to execute a query based on the condition tree would typically benefit from setting this parameter to <b>TRUE</b>.


### -param ppcResult [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>**</b>

Receives the address of a pointer to the new <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> node.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There are no special condition trees for <b>TRUE</b> and <b>FALSE</b>. However, a condition tree consisting of an AND node with no subconditions is always <b>TRUE</b>, and a condition tree consisting of an OR node with no subconditions is always <b>FALSE</b>. 




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>



<b>Reference</b>
 

 

