---
UID: NS:uiautomationcoreapi.UiaNotCondition
title: UiaNotCondition (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about a negative condition.helpviewer_keywords: ["UiaNotCondition","UiaNotCondition structure [Windows Accessibility]","uiauto.uiauto_UiaNotConditionStruct","uiauto_UiaNotConditionStruct","uiautomationcoreapi/UiaNotCondition","winauto.uiauto_UiaNotConditionStruct"]
old-location: winauto\uiauto_UiaNotConditionStruct.htm
tech.root: WinAuto
ms.assetid: 56f3f6b2-31b6-4eba-a6be-6a64f72e98df
ms.date: 12/05/2018
ms.keywords: UiaNotCondition, UiaNotCondition structure [Windows Accessibility], uiauto.uiauto_UiaNotConditionStruct, uiauto_UiaNotConditionStruct, uiautomationcoreapi/UiaNotCondition, winauto.uiauto_UiaNotConditionStruct
f1_keywords:
- uiautomationcoreapi/UiaNotCondition
dev_langs:
- c++
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- HeaderDef
api_location:
- UIAutomationCoreApi.h
api_name:
- UiaNotCondition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UiaNotCondition structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about a negative condition.


## -struct-fields




### -field ConditionType

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-conditiontype">ConditionType</a></b>

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-conditiontype">ConditionType</a> enumerated type indicating the type of condition.


### -field pCondition

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a>*</b>

The address of a <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a> structure containing information about the condition.

