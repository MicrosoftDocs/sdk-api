---
UID: NF:structuredquerycondition.ICondition.GetComparisonInfo
title: ICondition::GetComparisonInfo
author: windows-sdk-content
description: Retrieves the property name, operation, and value from a leaf search condition node.
old-location: search\_search_ICondition_GetComparisonInfo.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getcomparisoninfo.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetComparisonInfo, GetComparisonInfo method [search], GetComparisonInfo method [search],ICondition interface, ICondition interface [search],GetComparisonInfo method, ICondition.GetComparisonInfo, ICondition::GetComparisonInfo, _search_ICondition_GetComparisonInfo, search._search_ICondition_GetComparisonInfo, structuredquerycondition/ICondition::GetComparisonInfo
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
 - ICondition.GetComparisonInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- structuredquerycondition.h
: 
- ICondition.GetComparisonInfo
: 
---

# ICondition::GetComparisonInfo


## -description


Retrieves the property name, operation, and value from a leaf search condition node.
        


## -parameters




### -param ppszPropertyName [out, optional]

Type: <b>LPWSTR*</b>

Receives the name of the property of the leaf condition as a Unicode string.
                


### -param pcop [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>*</b>

Receives the operation of the leaf condition as a <a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a> enumeration.
                


### -param ppropvar [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Receives the value of the leaf condition as a <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.




## -remarks



Any or all of the three parameters can be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<b>Reference</b>
 

 

