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

# UiaCacheRequest structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about a request to cache data about UI Automation elements.


## -struct-fields




### -field pViewCondition

Type: <b>UiaCondition *</b>

The address of a <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structure that specifies the condition that cached elements must match.


### -field Scope

Type: <b><a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a></b>

A value from the <a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a> enumerated type indicating the scope of the cache request; for example, whether it includes children of the root element.


### -field pProperties

Type: <b>PROPERTYID*</b>

The address of an array of identifiers for properties to cache. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -field cProperties

Type: <b>int</b>

The count of elements in the <b>pProperties</b> array.


### -field pPatterns

Type: <b>PATTERNID*</b>

The address of an array of identifiers for control patterns to cache. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -field cPatterns

Type: <b>int</b>

The count of elements in the <b>pPatterns</b> array.


### -field automationElementMode

Type: <b><a href="https://msdn.microsoft.com/b0fadf47-2916-4555-b563-d0b5cd9056e6">AutomationElementMode</a></b>

A value from the <a href="https://msdn.microsoft.com/b0fadf47-2916-4555-b563-d0b5cd9056e6">AutomationElementMode</a> enumerated type indicating the type of reference to cached UI Automation elements that is to be returned.

