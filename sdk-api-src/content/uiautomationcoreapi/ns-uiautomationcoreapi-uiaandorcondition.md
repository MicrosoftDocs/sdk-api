---
UID: NS:uiautomationcoreapi.UiaAndOrCondition
title: UiaAndOrCondition (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about a complex condition.
helpviewer_keywords: ["UiaAndOrCondition","UiaAndOrCondition structure [Windows Accessibility]","uiauto.uiauto_UiaAndOrConditionStruct","uiauto_UiaAndOrConditionStruct","uiautomationcoreapi/UiaAndOrCondition","winauto.uiauto_UiaAndOrConditionStruct"]
old-location: winauto\uiauto_UiaAndOrConditionStruct.htm
tech.root: WinAuto
ms.assetid: de71d10e-ca81-4f66-a137-ae46adb47b4f
ms.date: 12/05/2018
ms.keywords: UiaAndOrCondition, UiaAndOrCondition structure [Windows Accessibility], uiauto.uiauto_UiaAndOrConditionStruct, uiauto_UiaAndOrConditionStruct, uiautomationcoreapi/UiaAndOrCondition, winauto.uiauto_UiaAndOrConditionStruct
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaAndOrCondition
 - uiautomationcoreapi/UiaAndOrCondition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaAndOrCondition
---

# UiaAndOrCondition structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about a complex condition.

## -struct-fields

### -field ConditionType

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-conditiontype">ConditionType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-conditiontype">ConditionType</a> enumerated type indicating the type of the condition.

### -field ppConditions

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a>**</b>

The address of an array of pointers to <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a> structures containing information about the complex condition.

### -field cConditions

Type: <b>int</b>

The count of elements in the <b>ppConditions</b> array.