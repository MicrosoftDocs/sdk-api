---
UID: NE:directmanipulation.DIRECTMANIPULATION_INTERACTION_TYPE
title: DIRECTMANIPULATION_INTERACTION_TYPE (directmanipulation.h)
description: Defines gestures recognized by Direct Manipulation.
helpviewer_keywords: ["DIRECTMANIPULATION_INTERACTION_BEGIN","DIRECTMANIPULATION_INTERACTION_END","DIRECTMANIPULATION_INTERACTION_TYPE","DIRECTMANIPULATION_INTERACTION_TYPE enumeration [Direct Manipulation]","DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_CROSS_SLIDE","DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_HOLD","DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_PINCH_ZOOM","DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_TAP","DIRECTMANIPULATION_INTERACTION_TYPE_MANIPULATION","directmanipulation.directmanipulation_interaction_type","directmanipulation/DIRECTMANIPULATION_INTERACTION_BEGIN","directmanipulation/DIRECTMANIPULATION_INTERACTION_END","directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE","directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_CROSS_SLIDE","directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_HOLD","directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_PINCH_ZOOM","directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_TAP","directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_MANIPULATION"]
old-location: directmanipulation\directmanipulation_interaction_type.htm
tech.root: directmanipulation
ms.assetid: 5C1C79C2-3407-4FF3-986F-D9BF51983A46
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_INTERACTION_BEGIN, DIRECTMANIPULATION_INTERACTION_END, DIRECTMANIPULATION_INTERACTION_TYPE, DIRECTMANIPULATION_INTERACTION_TYPE enumeration [Direct Manipulation], DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_CROSS_SLIDE, DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_HOLD, DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_PINCH_ZOOM, DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_TAP, DIRECTMANIPULATION_INTERACTION_TYPE_MANIPULATION, directmanipulation.directmanipulation_interaction_type, directmanipulation/DIRECTMANIPULATION_INTERACTION_BEGIN, directmanipulation/DIRECTMANIPULATION_INTERACTION_END, directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE, directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_CROSS_SLIDE, directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_HOLD, directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_PINCH_ZOOM, directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_TAP, directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE_MANIPULATION
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
req.typenames: DIRECTMANIPULATION_INTERACTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_INTERACTION_TYPE
 - directmanipulation/DIRECTMANIPULATION_INTERACTION_TYPE
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
 - DIRECTMANIPULATION_INTERACTION_TYPE
---

# DIRECTMANIPULATION_INTERACTION_TYPE enumeration


## -description

Defines gestures recognized by <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

## -enum-fields

### -field DIRECTMANIPULATION_INTERACTION_BEGIN:0

Marks the beginning of an interaction.

### -field DIRECTMANIPULATION_INTERACTION_TYPE_MANIPULATION:1

A compound gesture that supports translation, rotation and scaling.

### -field DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_TAP:2

A tap gesture.

### -field DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_HOLD:3

A hold gesture.

### -field DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_CROSS_SLIDE:4

Select or move through slide or swipe gestures.

### -field DIRECTMANIPULATION_INTERACTION_TYPE_GESTURE_PINCH_ZOOM:5

A zoom gesture.

### -field DIRECTMANIPULATION_INTERACTION_END:100

Marks the end of an interaction.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
