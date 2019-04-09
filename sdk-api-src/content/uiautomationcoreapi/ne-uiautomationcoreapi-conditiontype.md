---
UID: NE:uiautomationcoreapi.ConditionType
title: ConditionType (uiautomationcoreapi.h)
author: windows-sdk-content
description: Contains values that specify a type of UiaCondition.
old-location: winauto\uiauto_ConditionTypeEnum.htm
tech.root: WinAuto
ms.assetid: de69f8cd-bdbf-4636-ab14-b744a411acc5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ConditionType, ConditionType enumeration [Windows Accessibility], ConditionType_And, ConditionType_False, ConditionType_Not, ConditionType_Or, ConditionType_Property, ConditionType_True, uiauto.uiauto_ConditionTypeEnum, uiauto_ConditionTypeEnum, uiautomationcoreapi/ConditionType, uiautomationcoreapi/ConditionType_And, uiautomationcoreapi/ConditionType_False, uiautomationcoreapi/ConditionType_Not, uiautomationcoreapi/ConditionType_Or, uiautomationcoreapi/ConditionType_Property, uiautomationcoreapi/ConditionType_True, winauto.uiauto_ConditionTypeEnum
ms.topic: enum
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h
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
 - ConditionType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ConditionType enumeration


## -description


Contains values that specify a type of <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>.


## -enum-fields




### -field ConditionType_True

A condition that is true.


### -field ConditionType_False

A condition that is false.


### -field ConditionType_Property

A property condition.


### -field ConditionType_And

A complex condition where all the contained conditions must be true.


### -field ConditionType_Or

A complex condition where at least one of the contained conditions must be true.


### -field ConditionType_Not

A condition that is true if the specified conditions are not met.

