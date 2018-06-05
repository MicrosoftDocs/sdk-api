---
UID: NS:uiautomationcoreapi.UiaAndOrCondition
title: UiaAndOrCondition
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about a complex condition.
old-location: winauto\uiauto_UiaAndOrConditionStruct.htm
old-project: WinAuto
ms.assetid: de71d10e-ca81-4f66-a137-ae46adb47b4f
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaAndOrCondition, UiaAndOrCondition structure [Windows Accessibility], uiauto.uiauto_UiaAndOrConditionStruct, uiauto_UiaAndOrConditionStruct, uiautomationcoreapi/UiaAndOrCondition, winauto.uiauto_UiaAndOrConditionStruct
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAutomationCoreApi.h
api_name:
-	UiaAndOrCondition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaAndOrCondition structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about a complex condition.


## -struct-fields




### -field ConditionType

Type: <b><a href="https://msdn.microsoft.com/de69f8cd-bdbf-4636-ab14-b744a411acc5">ConditionType</a></b>

A value from the <a href="https://msdn.microsoft.com/de69f8cd-bdbf-4636-ab14-b744a411acc5">ConditionType</a> enumerated type indicating the type of the condition.


### -field ppConditions

Type: <b><a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>**</b>

The address of an array of pointers to <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structures containing information about the complex condition.


### -field cConditions

Type: <b>int</b>

The count of elements in the <b>ppConditions</b> array.

