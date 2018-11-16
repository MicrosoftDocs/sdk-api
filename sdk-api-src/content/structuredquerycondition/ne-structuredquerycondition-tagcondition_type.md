---
UID: NE:structuredquerycondition.tagCONDITION_TYPE
title: tagCONDITION_TYPE
author: windows-sdk-content
description: Provides a set of flags to be used with the following methods to indicate the type of condition tree node:\_ICondition::GetConditionType, IConditionFactory::MakeAndOr, IConditionFactory2::CreateCompoundFromArray, and IConditionFactory2::CreateCompoundFromObjectArray.
old-location: search\_search_CONDITION_TYPE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\condition_type.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CONDITION_TYPE, CONDITION_TYPE enumeration [search], CT_AND_CONDITION, CT_LEAF_CONDITION, CT_NOT_CONDITION, CT_OR_CONDITION, _search_CONDITION_TYPE, search._search_CONDITION_TYPE, structuredquerycondition/CONDITION_TYPE, structuredquerycondition/CT_AND_CONDITION, structuredquerycondition/CT_LEAF_CONDITION, structuredquerycondition/CT_NOT_CONDITION, structuredquerycondition/CT_OR_CONDITION, tagCONDITION_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquerycondition.h
api_name:
 - CONDITION_TYPE
product: Windows
targetos: Windows
req.typenames: CONDITION_TYPE
req.redist: Windows Desktop Search (WDS) 3.0
---

# tagCONDITION_TYPE enumeration


## -description


Provides a set of flags to be used with the following methods to indicate the type of condition tree node: 
        <a href="https://msdn.microsoft.com/ba2a2fa0-7d1e-4009-9c93-f620cc691b44">ICondition::GetConditionType</a>, 
        <a href="https://msdn.microsoft.com/b1446964-1fcd-4c94-ae9f-111abe55fa2d">IConditionFactory::MakeAndOr</a>, 
        <a href="https://msdn.microsoft.com/e360e7a3-a54c-4fb3-a34d-0a308b3d99de">IConditionFactory2::CreateCompoundFromArray</a>, and 
        <a href="https://msdn.microsoft.com/d707fbe2-f4c2-4746-985d-dd504d091de0">IConditionFactory2::CreateCompoundFromObjectArray</a>.


## -enum-fields




### -field CT_AND_CONDITION

Indicates that the values of the subterms are combined by "AND".


### -field CT_OR_CONDITION

Indicates that the values of the subterms are combined by "OR".


### -field CT_NOT_CONDITION

Indicates a "NOT" comparison of subterms.


### -field CT_LEAF_CONDITION

Indicates that the node is a comparison between a property and a constant value using a <a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>.


## -remarks



In Windows 7, this enumeration is defined in structuredquerycondition.idl and structuredquerycondition.h. Prior to Windows 7 this enumeration was declared in structuredquery.h and structuredquery.idl.

The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>



<a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>



<b>Reference</b>
 

 

