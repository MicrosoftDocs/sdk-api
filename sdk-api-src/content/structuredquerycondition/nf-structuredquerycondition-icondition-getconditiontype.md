---
UID: NF:structuredquerycondition.ICondition.GetConditionType
title: ICondition::GetConditionType (structuredquerycondition.h)
description: Retrieves the condition type for this search condition node, identifying it as a logical AND, OR, or NOT, or as a leaf node.
old-location: search\_search_ICondition_GetConditionType.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getconditiontype.htm
ms.date: 12/05/2018
ms.keywords: GetConditionType, GetConditionType method [search], GetConditionType method [search],ICondition interface, ICondition interface [search],GetConditionType method, ICondition.GetConditionType, ICondition::GetConditionType, _search_ICondition_GetConditionType, search._search_ICondition_GetConditionType, structuredquerycondition/ICondition::GetConditionType
f1_keywords:
- structuredquerycondition/ICondition.GetConditionType
dev_langs:
- c++
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
- ICondition.GetConditionType
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ICondition::GetConditionType


## -description


Retrieves the condition type for this search condition node, identifying it as a logical AND, OR, or NOT, or as a leaf node. 
        


## -parameters




### -param pNodeType [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>*</b>

Receives the <a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a> enumeration for this node.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The StructuredQuerySample code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting 
condition trees.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>
 

 

