---
UID: NE:structuredquerycondition.tagCONDITION_OPERATION
title: CONDITION_OPERATION
author: windows-sdk-content
description: Provides a set of flags to be used with following methods to indicate the operation in ICondition::GetComparisonInfo, ICondition2::GetLeafConditionInfo, IConditionFactory::MakeLeaf, IConditionFactory2::CreateBooleanLeaf, IConditionFactory2::CreateIntegerLeaf, IConditionFactory2::MakeLeaf, IConditionFactory2::CreateStringLeaf, and IConditionGenerator::GenerateForLeaf.
old-location: search\_search_CONDITION_OPERATION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\condition_operation.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CONDITION_OPERATION, CONDITION_OPERATION enumeration [search], COP_APPLICATION_SPECIFIC, COP_DOSWILDCARDS, COP_EQUAL, COP_GREATERTHAN, COP_GREATERTHANOREQUAL, COP_IMPLICIT, COP_LESSTHAN, COP_LESSTHANOREQUAL, COP_NOTEQUAL, COP_VALUE_CONTAINS, COP_VALUE_ENDSWITH, COP_VALUE_NOTCONTAINS, COP_VALUE_STARTSWITH, COP_WORD_EQUAL, COP_WORD_STARTSWITH, _search_CONDITION_OPERATION, search._search_CONDITION_OPERATION, structuredquerycondition/CONDITION_OPERATION, structuredquerycondition/COP_APPLICATION_SPECIFIC, structuredquerycondition/COP_DOSWILDCARDS, structuredquerycondition/COP_EQUAL, structuredquerycondition/COP_GREATERTHAN, structuredquerycondition/COP_GREATERTHANOREQUAL, structuredquerycondition/COP_IMPLICIT, structuredquerycondition/COP_LESSTHAN, structuredquerycondition/COP_LESSTHANOREQUAL, structuredquerycondition/COP_NOTEQUAL, structuredquerycondition/COP_VALUE_CONTAINS, structuredquerycondition/COP_VALUE_ENDSWITH, structuredquerycondition/COP_VALUE_NOTCONTAINS, structuredquerycondition/COP_VALUE_STARTSWITH, structuredquerycondition/COP_WORD_EQUAL, structuredquerycondition/COP_WORD_STARTSWITH
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
 - CONDITION_OPERATION
product: Windows
targetos: Windows
req.typenames: CONDITION_OPERATION
req.redist: Windows Desktop Search (WDS) 3.0
---

# CONDITION_OPERATION enumeration


## -description


Provides a set of flags to be used with following methods to indicate the operation in 
    <a href="https://msdn.microsoft.com/b87aa9dd-afed-4fe4-83e2-2a04d8ef2f0c">ICondition::GetComparisonInfo</a>, 
    <a href="https://msdn.microsoft.com/a7f3d491-3ddd-4bfe-84e0-a6f3a4c7946d">ICondition2::GetLeafConditionInfo</a>, 
    <a href="https://msdn.microsoft.com/aa2edf14-2176-411c-8139-2e270c21fa68">IConditionFactory::MakeLeaf</a>, 
    <a href="https://msdn.microsoft.com/db321ef5-2838-426b-8402-370ba19a887f">IConditionFactory2::CreateBooleanLeaf</a>, 
    <a href="https://msdn.microsoft.com/49ff5cf4-76e9-4ac0-82a2-6ae81c5ddcb1">IConditionFactory2::CreateIntegerLeaf</a>, 
    <a href="https://msdn.microsoft.com/e7cb9083-4ab9-4550-82e9-5c1da9c0f831">IConditionFactory2::MakeLeaf</a>, 
    <a href="https://msdn.microsoft.com/a59bf455-49cb-469a-860d-7ecd7dd94ec0">IConditionFactory2::CreateStringLeaf</a>, and 
    <a href="https://msdn.microsoft.com/940107e4-4f80-4eb8-8199-cfdfe989b8eb">IConditionGenerator::GenerateForLeaf</a>.        
         


## -enum-fields




### -field COP_IMPLICIT

An implicit comparison between the value of the property and the value of the constant. For an unresolved condition, <a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">COP_IMPLICIT</a> means that a user did not type an operation. In contrast, a resolved condition will always have a condition other than the <b>COP_IMPLICIT</b> operation.


### -field COP_EQUAL

The value of the property and the value of the constant must be equal.


### -field COP_NOTEQUAL

The value of the property and the value of the constant must not be equal.


### -field COP_LESSTHAN

The value of the property must be less than the value of the constant.


### -field COP_GREATERTHAN

The value of the property must be greater than the value of the constant.


### -field COP_LESSTHANOREQUAL

The value of the property must be less than or equal to the value of the constant.


### -field COP_GREATERTHANOREQUAL

The value of the property must be greater than or equal to the value of the constant.


### -field COP_VALUE_STARTSWITH

The value of the property must begin with the value of the constant.


### -field COP_VALUE_ENDSWITH

The value of the property must end with the value of the constant.


### -field COP_VALUE_CONTAINS

The value of the property must contain the value of the constant.


### -field COP_VALUE_NOTCONTAINS

The value of the property must not contain the value of the constant.


### -field COP_DOSWILDCARDS

The value of the property must match the value of the constant, where '?' matches any single character and '*' matches any sequence of characters.


### -field COP_WORD_EQUAL

The value of the property must contain a word that is the value of the constant.


### -field COP_WORD_STARTSWITH

The value of the property must contain a word that begins with the value of the constant.


### -field COP_APPLICATION_SPECIFIC

The application is free to interpret this in any suitable way.


## -remarks



Because a resolved condition never has a <b>COP_IMPLICIT</b> operation, applications that evaluate condition trees should not encounter it. However, <b>COP_IMPLICIT</b> could be used in comparing the output of either <a href="https://msdn.microsoft.com/b87aa9dd-afed-4fe4-83e2-2a04d8ef2f0c">ICondition::GetComparisonInfo</a> or <a href="https://msdn.microsoft.com/a7f3d491-3ddd-4bfe-84e0-a6f3a4c7946d">ICondition2::GetLeafConditionInfo</a> for a parsed unresolved condition to the output for a resolved condition.

In Windows 7, this enumeration is defined in structuredquerycondition.idl and structuredquerycondition.h. Prior to Windows 7 this enumeration was declared in structuredquery.h and structuredquery.idl.




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>



<a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>



<b>Reference</b>
 

 

