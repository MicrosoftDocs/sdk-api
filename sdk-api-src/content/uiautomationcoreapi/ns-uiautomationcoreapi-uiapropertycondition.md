---
UID: NS:uiautomationcoreapi.UiaPropertyCondition
title: UiaPropertyCondition (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about a condition used to find UI Automation elements that have a matching property.
helpviewer_keywords: ["UiaPropertyCondition","UiaPropertyCondition structure [Windows Accessibility]","uiauto.uiauto_UiaPropertyConditionStruct","uiauto_UiaPropertyConditionStruct","uiautomationcoreapi/UiaPropertyCondition","winauto.uiauto_UiaPropertyConditionStruct"]
old-location: winauto\uiauto_UiaPropertyConditionStruct.htm
tech.root: WinAuto
ms.assetid: 8a1ccd34-7839-4004-a663-0ce831c599f9
ms.date: 12/05/2018
ms.keywords: UiaPropertyCondition, UiaPropertyCondition structure [Windows Accessibility], uiauto.uiauto_UiaPropertyConditionStruct, uiauto_UiaPropertyConditionStruct, uiautomationcoreapi/UiaPropertyCondition, winauto.uiauto_UiaPropertyConditionStruct
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
 - UiaPropertyCondition
 - uiautomationcoreapi/UiaPropertyCondition
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
 - UiaPropertyCondition
---

# UiaPropertyCondition structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about a condition used to find UI Automation elements that have a matching property.

## -struct-fields

### -field ConditionType

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-conditiontype">ConditionType</a></b>

A value indicating the type of the condition.

### -field PropertyId

Type: <b>PROPERTYID</b>

The identifier of the property to match. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -field Value

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

The value that the property must have.

### -field Flags

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-propertyconditionflags">PropertyConditionFlags</a></b>

A value indicating how the condition is applied.