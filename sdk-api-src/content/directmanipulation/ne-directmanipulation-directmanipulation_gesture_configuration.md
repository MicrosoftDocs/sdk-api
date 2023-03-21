---
UID: NE:directmanipulation.DIRECTMANIPULATION_GESTURE_CONFIGURATION
title: DIRECTMANIPULATION_GESTURE_CONFIGURATION (directmanipulation.h)
description: Defines the gestures that can be passed to SetManualGesture.
helpviewer_keywords: ["DIRECTMANIPULATION_GESTURE_CONFIGURATION","DIRECTMANIPULATION_GESTURE_CONFIGURATION enumeration [Direct Manipulation]","DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_HORIZONTAL","DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_VERTICAL","DIRECTMANIPULATION_GESTURE_DEFAULT","DIRECTMANIPULATION_GESTURE_NONE","DIRECTMANIPULATION_GESTURE_PINCH_ZOOM","directmanipulation.directmanipulation_gesture_configuration","directmanipulation/DIRECTMANIPULATION_GESTURE_CONFIGURATION","directmanipulation/DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_HORIZONTAL","directmanipulation/DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_VERTICAL","directmanipulation/DIRECTMANIPULATION_GESTURE_DEFAULT","directmanipulation/DIRECTMANIPULATION_GESTURE_NONE","directmanipulation/DIRECTMANIPULATION_GESTURE_PINCH_ZOOM"]
old-location: directmanipulation\directmanipulation_gesture_configuration.htm
tech.root: directmanipulation
ms.assetid: B8EE991B-6DBF-42DE-966F-FA5CB397562C
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_GESTURE_CONFIGURATION, DIRECTMANIPULATION_GESTURE_CONFIGURATION enumeration [Direct Manipulation], DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_HORIZONTAL, DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_VERTICAL, DIRECTMANIPULATION_GESTURE_DEFAULT, DIRECTMANIPULATION_GESTURE_NONE, DIRECTMANIPULATION_GESTURE_PINCH_ZOOM, directmanipulation.directmanipulation_gesture_configuration, directmanipulation/DIRECTMANIPULATION_GESTURE_CONFIGURATION, directmanipulation/DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_HORIZONTAL, directmanipulation/DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_VERTICAL, directmanipulation/DIRECTMANIPULATION_GESTURE_DEFAULT, directmanipulation/DIRECTMANIPULATION_GESTURE_NONE, directmanipulation/DIRECTMANIPULATION_GESTURE_PINCH_ZOOM
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIRECTMANIPULATION_GESTURE_CONFIGURATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_GESTURE_CONFIGURATION
 - directmanipulation/DIRECTMANIPULATION_GESTURE_CONFIGURATION
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
 - DIRECTMANIPULATION_GESTURE_CONFIGURATION
---

# DIRECTMANIPULATION_GESTURE_CONFIGURATION enumeration


## -description

Defines the gestures that can be passed to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setmanualgesture">SetManualGesture</a>.

## -enum-fields

### -field DIRECTMANIPULATION_GESTURE_NONE:0

No gestures are defined.

### -field DIRECTMANIPULATION_GESTURE_DEFAULT:0

Only default gestures are supported. This is the default value.

### -field DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_VERTICAL:0x8

Vertical slide and swipe gestures are supported through the cross-slide interaction. For more information, see <a href="/windows/uwp/input-and-devices/guidelines-for-cross-slide">Guidelines for cross-slide</a>.

### -field DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_HORIZONTAL:0x10

Horizontal slide and swipe gestures are supported through the cross-slide interaction. For more information, see <a href="/windows/uwp/input-and-devices/guidelines-for-cross-slide">Guidelines for cross-slide</a>.

### -field DIRECTMANIPULATION_GESTURE_PINCH_ZOOM:0x20

Pinch and stretch gestures for zooming.

## -remarks

By default, <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> always reassigns tap and press-and-hold gestures to the application. 


Use <b>DIRECTMANIPULATION_GESTURE_PINCH_ZOOM</b> to zoom instead of scale.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
