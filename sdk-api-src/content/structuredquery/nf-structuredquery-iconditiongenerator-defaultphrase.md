---
UID: NF:structuredquery.IConditionGenerator.DefaultPhrase
title: IConditionGenerator::DefaultPhrase
author: windows-sdk-content
description: This method attempts to produce a phrase that, when recognized by this instance of IConditionGenerator, represents the type and value pair for an entity, relationship, or named entity.
old-location: search\_search_IConditionGenerator_DefaultPhrase.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\defaultphrase.htm
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DefaultPhrase, DefaultPhrase method [search], DefaultPhrase method [search],IConditionGenerator interface, IConditionGenerator interface [search],DefaultPhrase method, IConditionGenerator.DefaultPhrase, IConditionGenerator::DefaultPhrase, _search_IConditionGenerator_DefaultPhrase, search._search_IConditionGenerator_DefaultPhrase, structuredquery/IConditionGenerator::DefaultPhrase
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
 - IConditionGenerator.DefaultPhrase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConditionGenerator::DefaultPhrase


## -description


This method attempts to produce a phrase that, when recognized by this instance of <a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>, represents the type and value pair for an entity, relationship, or named entity.


## -parameters




### -param pszValueType [in]

Type: <b>LPCWSTR</b>

The semantic type of the value in <i>ppropvar</i>.


### -param ppropvar

TBD


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
 

 

