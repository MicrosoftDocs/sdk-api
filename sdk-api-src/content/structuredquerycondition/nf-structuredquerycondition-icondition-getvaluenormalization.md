---
UID: NF:structuredquerycondition.ICondition.GetValueNormalization
title: ICondition::GetValueNormalization method
author: windows-driver-content
description: Retrieves the character-normalized value of the search condition node.
old-location: search\_search_ICondition_GetValueNormalization.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getvaluenormalization.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetValueNormalization method [search], GetValueNormalization method [search], ICondition interface, GetValueNormalization,ICondition.GetValueNormalization, ICondition, ICondition interface [search], GetValueNormalization method, ICondition::GetValueNormalization, _search_ICondition_GetValueNormalization, search._search_ICondition_GetValueNormalization, structuredquerycondition/ICondition::GetValueNormalization
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
req.typenames: CONDITION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	structuredquerycondition.h
api_name:
-	ICondition.GetValueNormalization
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ICondition::GetValueNormalization method


## -description



          Retrieves the character-normalized value of the search condition node.
        


## -parameters




### -param ppszNormalization [out, retval]

Type: <b>LPWSTR*</b>


                    Receives a pointer to a Unicode string representation of the value.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.




## -remarks



In <b>Windows 7 and later</b>, if the value of the leaf node is <b>VT_EMPTY</b>, <i>ppwszNormalization</i> points to an empty string. If the value is a string, such as VT_LPWSTR, VT_BSTR or VT_LPSTR, then <i>ppwszNormalization</i> is set to a character-normalized form of the value. In other cases, <i>ppwszNormalization</i> is set to some other character-normalized string representation of the value.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<b>Reference</b>
 

 

