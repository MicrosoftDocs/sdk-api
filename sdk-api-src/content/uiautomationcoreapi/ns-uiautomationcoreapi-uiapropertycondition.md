---
UID: NS:uiautomationcoreapi.UiaPropertyCondition
title: UiaPropertyCondition
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about a condition used to find UI Automation elements that have a matching property.
old-location: winauto\uiauto_UiaPropertyConditionStruct.htm
tech.root: WinAuto
ms.assetid: 8a1ccd34-7839-4004-a663-0ce831c599f9
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: UiaPropertyCondition, UiaPropertyCondition structure [Windows Accessibility], uiauto.uiauto_UiaPropertyConditionStruct, uiauto_UiaPropertyConditionStruct, uiautomationcoreapi/UiaPropertyCondition, winauto.uiauto_UiaPropertyConditionStruct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - UiaPropertyCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaPropertyCondition structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about a condition used to find UI Automation elements that have a matching property.


## -struct-fields




### -field ConditionType

Type: <b><a href="https://msdn.microsoft.com/de69f8cd-bdbf-4636-ab14-b744a411acc5">ConditionType</a></b>

A value indicating the type of the condition.


### -field PropertyId

Type: <b>PROPERTYID</b>

The identifier of the property to match. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -field Value

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The value that the property must have.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/debe8141-2a91-4774-b533-d6f3ccfc7744">PropertyConditionFlags</a></b>

A value indicating how the condition is applied.

