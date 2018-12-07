---
UID: NF:structuredquery.IConditionGenerator.DefaultPhrase
title: IConditionGenerator::DefaultPhrase
author: windows-sdk-content
description: This method attempts to produce a phrase that, when recognized by this instance of IConditionGenerator, represents the type and value pair for an entity, relationship, or named entity.
old-location: search\_search_IConditionGenerator_DefaultPhrase.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\defaultphrase.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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


This method attempts to produce a phrase that, when recognized by this instance of <a href="https://msdn.microsoft.com/en-us/library/Bb231380(v=VS.85).aspx">IConditionGenerator</a>, represents the type and value pair for an entity, relationship, or named entity.


## -parameters




### -param pszValueType [in]

Type: <b>LPCWSTR</b>

The semantic type of the value in <i>ppropvar</i>.


### -param ppropvar [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT const</a>*</b>

The value to be processed.


### -param fUseEnglish [in]

Type: <b>BOOL</b>

 The parameter fUseEnglish is reserved: it should be ignored by implementors, and callers should pass <b>FALSE</b>.


### -param ppszPhrase [out, retval, optional]

Type: <b>LPWSTR*</b>

Receives a pointer to the phrase representing the value. If no phrase can be produced, this parameter is set to <b>NULL</b> and the method returns S_FALSE.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if the input arguments are valid but no phrase can be produced, and an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231380(v=VS.85).aspx">IConditionGenerator</a>



<b>Reference</b>
 

 

