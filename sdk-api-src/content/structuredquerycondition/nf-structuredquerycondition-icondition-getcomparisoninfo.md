---
UID: NF:structuredquerycondition.ICondition.GetComparisonInfo
title: ICondition::GetComparisonInfo (structuredquerycondition.h)
author: windows-sdk-content
description: Retrieves the property name, operation, and value from a leaf search condition node.
old-location: search\_search_ICondition_GetComparisonInfo.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getcomparisoninfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetComparisonInfo, GetComparisonInfo method [search], GetComparisonInfo method [search],ICondition interface, ICondition interface [search],GetComparisonInfo method, ICondition.GetComparisonInfo, ICondition::GetComparisonInfo, _search_ICondition_GetComparisonInfo, search._search_ICondition_GetComparisonInfo, structuredquerycondition/ICondition::GetComparisonInfo
ms.topic: method
f1_keywords: 
 - "structuredquerycondition/ICondition.GetComparisonInfo"
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
ms.custom: 19H1
---

# ICondition::GetComparisonInfo


## -description


Retrieves the property name, operation, and value from a leaf search condition node.
        


## -parameters




### -param ppszPropertyName [out, optional]

Type: <b>LPWSTR*</b>

Receives the name of the property of the leaf condition as a Unicode string.
                


### -param pcop [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/ne-structuredquerycondition-tagcondition_operation">CONDITION_OPERATION</a>*</b>

Receives the operation of the leaf condition as a <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/ne-structuredquerycondition-tagcondition_operation">CONDITION_OPERATION</a> enumeration.
                


### -param ppropvar [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>*</b>

Receives the value of the leaf condition as a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.




## -remarks



Any or all of the three parameters can be <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/ne-structuredquerycondition-tagcondition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/ne-structuredquerycondition-tagcondition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>
 

 

