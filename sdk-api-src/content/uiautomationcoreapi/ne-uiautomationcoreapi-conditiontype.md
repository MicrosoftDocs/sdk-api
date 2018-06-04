---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

