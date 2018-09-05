---
UID: NF:structuredquery.IConditionGenerator.Initialize
title: IConditionGenerator::Initialize
author: windows-sdk-content
description: Resets all states of the interface to default values and retrieves any necessary information from the schema.
old-location: search\_search_IConditionGenerator_Initialize.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\initialize.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IConditionGenerator interface [search],Initialize method, IConditionGenerator.Initialize, IConditionGenerator::Initialize, Initialize, Initialize method [search], Initialize method [search],IConditionGenerator interface, _search_IConditionGenerator_Initialize, search._search_IConditionGenerator_Initialize, structuredquery/IConditionGenerator::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.redist: 
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
 - IConditionGenerator.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionGenerator::Initialize


## -description


Resets all states of the interface to default values and retrieves any necessary information from the schema.
        


## -parameters




### -param pSchemaProvider [in]

Type: <b><a href="https://msdn.microsoft.com/c6cb1da0-5072-41b2-aa64-e39c8c97b2f8">ISchemaProvider</a>*</b>

Pointer to the schema to be used.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>



<b>Reference</b>
 

 

