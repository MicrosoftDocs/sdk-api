---
UID: NE:interactioncontext.CROSS_SLIDE_FLAGS
title: CROSS_SLIDE_FLAGS
author: windows-driver-content
description: Specifies the state of the cross-slide interaction.
old-location: input_intcontext\cross_slide_flags.htm
old-project: Input_IntContext
ms.assetid: 3be72ad1-87da-4c08-84fd-a84d4c03d33b
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: CROSS_SLIDE_FLAGS, CROSS_SLIDE_FLAGS enumeration, CROSS_SLIDE_FLAGS_MAX, CROSS_SLIDE_FLAGS_NONE, CROSS_SLIDE_FLAGS_REARRANGE, CROSS_SLIDE_FLAGS_SELECT, CROSS_SLIDE_FLAGS_SPEED_BUMP, input_intcontext.cross_slide_flags, interactioncontext.cross_slide_flags, interactioncontext/CROSS_SLIDE_FLAGS, interactioncontext/CROSS_SLIDE_FLAGS_MAX, interactioncontext/CROSS_SLIDE_FLAGS_NONE, interactioncontext/CROSS_SLIDE_FLAGS_REARRANGE, interactioncontext/CROSS_SLIDE_FLAGS_SELECT, interactioncontext/CROSS_SLIDE_FLAGS_SPEED_BUMP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CROSS_SLIDE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	interactioncontext.h
api_name:
-	CROSS_SLIDE_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CROSS_SLIDE_FLAGS enumeration


## -description


Specifies the state of the cross-slide interaction.


## -enum-fields




### -field CROSS_SLIDE_FLAGS_NONE

No cross-slide interaction.


### -field CROSS_SLIDE_FLAGS_SELECT

Cross-slide interaction has crossed a distance threshold and is in select mode.


### -field CROSS_SLIDE_FLAGS_SPEED_BUMP

Cross-slide interaction is in speed bump mode.


### -field CROSS_SLIDE_FLAGS_REARRANGE

Cross-slide interaction has crossed the speed bump threshold and is in rearrange (drag and drop) mode.


### -field CROSS_SLIDE_FLAGS_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/365b0bed-888e-4e9c-ad13-254a241b9de9">INTERACTION_ARGUMENTS_CROSS_SLIDE</a>



<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>
 

 

