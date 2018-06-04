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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a></b>

The value that the property must have.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/debe8141-2a91-4774-b533-d6f3ccfc7744">PropertyConditionFlags</a></b>

A value indicating how the condition is applied.

