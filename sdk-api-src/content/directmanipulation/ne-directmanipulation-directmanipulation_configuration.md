---
UID: NE:directmanipulation.DIRECTMANIPULATION_CONFIGURATION
title: DIRECTMANIPULATION_CONFIGURATION
author: windows-driver-content
description: Defines the interaction configuration states available in Direct Manipulation.
old-location: directmanipulation\directmanipulation_configuration.htm
old-project: directmanipulation
ms.assetid: a7c146e8-a1df-4445-8230-1dd491d0e9a3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: DIRECTMANIPULATION_CONFIGURATION, DIRECTMANIPULATION_CONFIGURATION enumeration [Direct Manipulation], DIRECTMANIPULATION_CONFIGURATION_INTERACTION, DIRECTMANIPULATION_CONFIGURATION_NONE, DIRECTMANIPULATION_CONFIGURATION_RAILS_X, DIRECTMANIPULATION_CONFIGURATION_RAILS_Y, DIRECTMANIPULATION_CONFIGURATION_SCALING, DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA, DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA, DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X, DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y, directmanipulation.directmanipulation_configuration, directmanipulation/DIRECTMANIPULATION_CONFIGURATION, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_INTERACTION, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_NONE, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_RAILS_X, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_RAILS_Y, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_SCALING, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DIRECTMANIPULATION_CONFIGURATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	directmanipulation.h
api_name:
-	DIRECTMANIPULATION_CONFIGURATION
product: Windows
targetos: Windows
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
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
 

 

