---
UID: NF:structuredquerycondition.ICondition.GetValueType
title: ICondition::GetValueType
author: windows-sdk-content
description: Retrieves the semantic type of the value of the search condition node.
old-location: search\_search_ICondition_GetValueType.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getvaluetype.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetValueType, GetValueType method [search], GetValueType method [search],ICondition interface, ICondition interface [search],GetValueType method, ICondition.GetValueType, ICondition::GetValueType, _search_ICondition_GetValueType, search._search_ICondition_GetValueType, structuredquerycondition/ICondition::GetValueType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquerycondition.h
req.include-header: Structuredquery.h
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
 - structuredquerycondition.h
api_name:
 - ICondition.GetValueType
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ICondition::GetValueType


## -description


Retrieves the semantic type of the value of the search condition node.
        


## -parameters




### -param ppszValueTypeName [out, retval]

Type: <b>LPWSTR*</b>

Receives either a pointer to the semantic type of the value as a Unicode string or <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.
                




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<b>Reference</b>
 

 

