---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0001
title: InteractionMode (peninputpanel.h)
description: Specifies the interaction modes that can be chosen by the user for the Tablet PC Input Panel.
helpviewer_keywords: ["8e01c1fd-3351-47f1-beae-c84d9f7969a8","InteractionMode","InteractionMode enumeration [Tablet PC]","InteractionMode_DockedBottom","InteractionMode_DockedTop","InteractionMode_Floating","InteractionMode_InPlace","peninputpanel/InteractionMode","peninputpanel/InteractionMode_DockedBottom","peninputpanel/InteractionMode_DockedTop","peninputpanel/InteractionMode_Floating","peninputpanel/InteractionMode_InPlace","tablet.interactionmode"]
old-location: tablet\interactionmode.htm
tech.root: tablet
ms.assetid: 8e01c1fd-3351-47f1-beae-c84d9f7969a8
ms.date: 12/05/2018
ms.keywords: 8e01c1fd-3351-47f1-beae-c84d9f7969a8, InteractionMode, InteractionMode enumeration [Tablet PC], InteractionMode_DockedBottom, InteractionMode_DockedTop, InteractionMode_Floating, InteractionMode_InPlace, peninputpanel/InteractionMode, peninputpanel/InteractionMode_DockedBottom, peninputpanel/InteractionMode_DockedTop, peninputpanel/InteractionMode_Floating, peninputpanel/InteractionMode_InPlace, tablet.interactionmode
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
targetos: Windows
req.typenames: InteractionMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_peninputpanel_0000_0000_0001
 - peninputpanel/__MIDL___MIDL_itf_peninputpanel_0000_0000_0001
 - InteractionMode
 - peninputpanel/InteractionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peninputpanel.h
api_name:
 - InteractionMode
---

# InteractionMode enumeration


## -description

Specifies the interaction modes that can be chosen by the user for the Tablet PC Input Panel.

## -enum-fields

### -field InteractionMode_InPlace:0

The Input Panel appears next to the text insertion point that currently has focus.

### -field InteractionMode_Floating:1

The Input Panel is not tied to an insertion point. The Floating Input Panel is opened by tapping on the Input Panel tab which appears by default on the left edge of the screen. The positioning and control of the Input Panel is left entirely to the user.

### -field InteractionMode_DockedTop:2

The Input Panel appears at the top of the screen and the active desktop is resized so that the Input Panel does not overlap with any other windows or UI elements.

### -field InteractionMode_DockedBottom:3

The Input Panel appears at the bottom of the screen and the active desktop is resized so that the Input Panel does not overlap with any other windows or UI elements.

