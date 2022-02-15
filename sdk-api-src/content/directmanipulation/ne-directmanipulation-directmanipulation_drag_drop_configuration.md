---
UID: NE:directmanipulation.DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION
title: DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION (directmanipulation.h)
description: Defines behaviors for the drag-drop interaction.
helpviewer_keywords: ["DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION","DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION enumeration [Direct Manipulation]","DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG","DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL","DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG","DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY","DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL","directmanipulation.directmanipulation_drag_drop_configuration","directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION","directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG","directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL","directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG","directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY","directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL"]
old-location: directmanipulation\directmanipulation_drag_drop_configuration.htm
tech.root: directmanipulation
ms.assetid: F41BD870-002B-4627-85EA-8064B156611D
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION, DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION enumeration [Direct Manipulation], DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG, DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL, DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG, DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY, DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL, directmanipulation.directmanipulation_drag_drop_configuration, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION
 - directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION
---

# DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION enumeration


## -description

Defines behaviors for the drag-drop interaction.

## -enum-fields

### -field DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL:0x1

Specifies that vertical movement is applicable to the chosen gesture.

### -field DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL:0x2

Specifies that horizontal movement is applicable to the chosen gesture.

### -field DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY:0x10

Specifies that the gesture is to be cross-slide only.

### -field DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG:0x20

Specifies that the gesture is a drag initiated by cross-slide.

### -field DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG:0x40

Specifies that the gesture a drag initiated by press-and-hold.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
