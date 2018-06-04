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

# __MIDL___MIDL_itf_peninputpanel_0000_0000_0001 enumeration


## -description



Specifies the interaction modes that can be chosen by the user for the Tablet PC Input Panel.




## -enum-fields




### -field InteractionMode_InPlace

The Input Panel appears next to the text insertion point that currently has focus.


### -field InteractionMode_Floating

The Input Panel is not tied to an insertion point. The Floating Input Panel is opened by tapping on the Input Panel tab which appears by default on the left edge of the screen. The positioning and control of the Input Panel is left entirely to the user.


### -field InteractionMode_DockedTop

The Input Panel appears at the top of the screen and the active desktop is resized so that the Input Panel does not overlap with any other windows or UI elements.


### -field InteractionMode_DockedBottom

The Input Panel appears at the bottom of the screen and the active desktop is resized so that the Input Panel does not overlap with any other windows or UI elements.

