---
UID: NF:structuredquerycondition.ICondition2.GetLocale
title: ICondition2::GetLocale
author: windows-sdk-content
description: Retrieves the property name, operation, and value from a leaf search condition node.
old-location: search\_search_ICondition2_GetLocale.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\icondition2\getlocale.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetLocale, GetLocale method [search], GetLocale method [search],ICondition2 interface, ICondition2 interface [search],GetLocale method, ICondition2.GetLocale, ICondition2::GetLocale, _search_ICondition2_GetLocale, search._search_ICondition2_GetLocale, structuredquerycondition/ICondition2::GetLocale
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - ICondition2.GetLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICondition2::GetLocale


## -description


Retrieves the property name, operation, and value from a leaf search condition node.
        


## -parameters




### -param ppszLocaleName [out, optional]

Type: <b>LPWSTR*</b>

Receives the name of the locale of the leaf condition as a Unicode string. This parameter can be <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

                    Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<b>Reference</b>
 

 

