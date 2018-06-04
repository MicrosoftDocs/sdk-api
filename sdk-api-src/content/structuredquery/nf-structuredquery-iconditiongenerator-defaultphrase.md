---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IConditionGenerator::DefaultPhrase


## -description


This method attempts to produce a phrase that, when recognized by this instance of <a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>, represents the type and value pair for an entity, relationship, or named entity.


## -parameters




### -param pszValueType [in]

Type: <b>LPCWSTR</b>

The semantic type of the value in <i>ppropvar</i>.


### -param ppropvar




### -param fUseEnglish [in]

Type: <b>BOOL</b>

 The parameter fUseEnglish is reserved: it should be ignored by implementors, and callers should pass <b>FALSE</b>.


### -param ppszPhrase [out, retval, optional]

Type: <b>LPWSTR*</b>

Receives a pointer to the phrase representing the value. If no phrase can be produced, this parameter is set to <b>NULL</b> and the method returns S_FALSE.


#### - pPropVar [in]

Type: <b><a href="_stg_propvariant">PROPVARIANT const</a>*</b>

The value to be processed.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if the input arguments are valid but no phrase can be produced, and an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>



<b>Reference</b>
 

 

