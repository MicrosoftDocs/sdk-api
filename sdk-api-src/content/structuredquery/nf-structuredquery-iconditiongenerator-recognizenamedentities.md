---
UID: NF:structuredquery.IConditionGenerator.RecognizeNamedEntities
title: IConditionGenerator::RecognizeNamedEntities
author: windows-sdk-content
description: Identifies named entities in an input string, and creates a collection containing them.
old-location: search\_search_IConditionGenerator_RecognizeNamedEntities.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\recognizenamedentities.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IConditionGenerator interface [search],RecognizeNamedEntities method, IConditionGenerator.RecognizeNamedEntities, IConditionGenerator::RecognizeNamedEntities, RecognizeNamedEntities, RecognizeNamedEntities method [search], RecognizeNamedEntities method [search],IConditionGenerator interface, _search_IConditionGenerator_RecognizeNamedEntities, search._search_IConditionGenerator_RecognizeNamedEntities, structuredquery/IConditionGenerator::RecognizeNamedEntities
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
 - IConditionGenerator.RecognizeNamedEntities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConditionGenerator::RecognizeNamedEntities


## -description


Identifies named entities in an input string, and creates a collection containing them. The value of each named entity is expressed as a string, which is then used by <a href="https://msdn.microsoft.com/940107e4-4f80-4eb8-8199-cfdfe989b8eb">IConditionGenerator::GenerateForLeaf</a>. The string can contain any data and be in any format, because it is not examined by any other components.
	    


## -parameters




### -param pszInputString [in]

Type: <b>LPCWSTR</b>

The input string to be parsed.
            


### -param lcidUserLocale [in]

Type: <b>LCID</b>

The LCID against which named entities should be recognized.
            


### -param pTokenCollection [in]

Type: <b><a href="https://msdn.microsoft.com/e7f5b3ce-dae2-41ec-90ff-9ab49e0301bd">ITokenCollection</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e7f5b3ce-dae2-41ec-90ff-9ab49e0301bd">ITokenCollection</a> object that indicates how the input string was tokenized.
            


### -param pNamedEntities [in, out]

Type: <b><a href="https://msdn.microsoft.com/0ed17267-38e0-4a01-ab72-fbf1cb860300">INamedEntityCollector</a>*</b>

On input, contains an <a href="https://msdn.microsoft.com/0ed17267-38e0-4a01-ab72-fbf1cb860300">INamedEntityCollector</a> or <b>NULL</b>. On return, contains an <b>INamedEntityCollector</b> collection of the named entities.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Given an input string, a user locale (typically the user's default locale) and a tokenization of the input string, the <b>IConditionGenerator::RecognizeNamedEntities</b> method should be able to identify any named entities in that input string, and then add each entity to the named entity collection.     
            




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>



<b>Reference</b>
 

 

