---
UID: NF:structuredquerycondition.ICondition.GetComparisonInfo
title: ICondition::GetComparisonInfo method
author: windows-driver-content
description: Retrieves the property name, operation, and value from a leaf search condition node.
old-location: search\_search_ICondition_GetComparisonInfo.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getcomparisoninfo.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetComparisonInfo method [search], GetComparisonInfo method [search], ICondition interface, GetComparisonInfo,ICondition.GetComparisonInfo, ICondition, ICondition interface [search], GetComparisonInfo method, ICondition::GetComparisonInfo, _search_ICondition_GetComparisonInfo, search._search_ICondition_GetComparisonInfo, structuredquerycondition/ICondition::GetComparisonInfo
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
-	ICondition.GetComparisonInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ICondition::GetComparisonInfo method


## -description



          Retrieves the property name, operation, and value from a leaf search condition node.
        


## -parameters




### -param ppszPropertyName [out, optional]

Type: <b>LPWSTR*</b>


                    Receives the name of the property of the leaf condition as a Unicode string.
                


### -param pcop [out, optional]

Type: <b><a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>*</b>


                    Receives the operation of the leaf condition as a <a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a> enumeration.
                


### -param ppropvar [out, optional]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>


                    Receives the value of the leaf condition as a <a href="_stg_propvariant">PROPVARIANT</a>.
                


## -returns



Type: <b>HRESULT</b>


                    Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.




## -remarks



Any or all of the three parameters can be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<b>Reference</b>
 

 

