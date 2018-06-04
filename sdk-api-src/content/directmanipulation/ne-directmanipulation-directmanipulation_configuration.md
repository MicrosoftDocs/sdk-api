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

# DIRECTMANIPULATION_CONFIGURATION enumeration


## -description


Defines the interaction configuration states available in <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>.


## -enum-fields




### -field DIRECTMANIPULATION_CONFIGURATION_NONE

No interaction is defined.


### -field DIRECTMANIPULATION_CONFIGURATION_INTERACTION

An interaction is defined. To enable interactions, this value must be included.

Required when setting a configuration other than <b>DIRECTMANIPULATION_CONFIGURATION_NONE</b>.


### -field DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X

Translation in the horizontal axis.


### -field DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y

Translation in the vertical axis.


### -field DIRECTMANIPULATION_CONFIGURATION_SCALING

Zoom.


### -field DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA

Inertia for translation as defined by <b>DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X</b> and <b>DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y</b>.


### -field DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA

Inertia for zoom as defined by <b>DIRECTMANIPULATION_CONFIGURATION _SCALING</b>.


### -field DIRECTMANIPULATION_CONFIGURATION_RAILS_X

Rails on the horizontal axis.


### -field DIRECTMANIPULATION_CONFIGURATION_RAILS_Y

Rails on the vertical axis.


## -see-also




<a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>



<a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>



<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>



<a href="https://msdn.microsoft.com/2aac9468-a060-4f06-9e8e-139355be75f7">RemoveConfiguration</a>
 

 

