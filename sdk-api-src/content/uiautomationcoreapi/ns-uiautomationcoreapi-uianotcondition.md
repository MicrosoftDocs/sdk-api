---
UID: NS:uiautomationcoreapi.UiaNotCondition
title: UiaNotCondition
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about a negative condition.
old-location: winauto\uiauto_UiaNotConditionStruct.htm
tech.root: WinAuto
ms.assetid: 56f3f6b2-31b6-4eba-a6be-6a64f72e98df
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: UiaNotCondition, UiaNotCondition structure [Windows Accessibility], uiauto.uiauto_UiaNotConditionStruct, uiauto_UiaNotConditionStruct, uiautomationcoreapi/UiaNotCondition, winauto.uiauto_UiaNotConditionStruct
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
 - UiaNotCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaNotCondition structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about a negative condition.


## -struct-fields




### -field ConditionType

Type: <b><a href="https://msdn.microsoft.com/de69f8cd-bdbf-4636-ab14-b744a411acc5">ConditionType</a></b>

A value from the <a href="https://msdn.microsoft.com/de69f8cd-bdbf-4636-ab14-b744a411acc5">ConditionType</a> enumerated type indicating the type of condition.


### -field pCondition

Type: <b><a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>*</b>

The address of a <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structure containing information about the condition.

