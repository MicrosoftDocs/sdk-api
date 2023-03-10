---
UID: NE:msinkaut.InkSystemGesture
title: InkSystemGesture (msinkaut.h)
description: Specifies the interest in a set of operating system-specific gestures.
helpviewer_keywords: ["213c8a44-1313-47cf-8703-3e9ed5e36d33","ISG_DoubleTap","ISG_Drag","ISG_Flick","ISG_HoldEnter","ISG_HoldLeave","ISG_HoverEnter","ISG_HoverLeave","ISG_RightDrag","ISG_RightTap","ISG_Tap","InkSystemGesture","InkSystemGesture enumeration [Tablet PC]","msinkaut/ISG_DoubleTap","msinkaut/ISG_Drag","msinkaut/ISG_Flick","msinkaut/ISG_HoldEnter","msinkaut/ISG_HoldLeave","msinkaut/ISG_HoverEnter","msinkaut/ISG_HoverLeave","msinkaut/ISG_RightDrag","msinkaut/ISG_RightTap","msinkaut/ISG_Tap","msinkaut/InkSystemGesture","tablet.inksystemgesture"]
old-location: tablet\inksystemgesture.htm
tech.root: tablet
ms.assetid: 213c8a44-1313-47cf-8703-3e9ed5e36d33
ms.date: 12/05/2018
ms.keywords: 213c8a44-1313-47cf-8703-3e9ed5e36d33, ISG_DoubleTap, ISG_Drag, ISG_Flick, ISG_HoldEnter, ISG_HoldLeave, ISG_HoverEnter, ISG_HoverLeave, ISG_RightDrag, ISG_RightTap, ISG_Tap, InkSystemGesture, InkSystemGesture enumeration [Tablet PC], msinkaut/ISG_DoubleTap, msinkaut/ISG_Drag, msinkaut/ISG_Flick, msinkaut/ISG_HoldEnter, msinkaut/ISG_HoldLeave, msinkaut/ISG_HoverEnter, msinkaut/ISG_HoverLeave, msinkaut/ISG_RightDrag, msinkaut/ISG_RightTap, msinkaut/ISG_Tap, msinkaut/InkSystemGesture, tablet.inksystemgesture
req.header: msinkaut.h
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
req.typenames: InkSystemGesture
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkSystemGesture
 - msinkaut/InkSystemGesture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkSystemGesture
---

# InkSystemGesture enumeration


## -description

Specifies the interest in a set of operating system-specific gestures.

## -enum-fields

### -field ISG_Tap:0x10

A click of the left mouse button. This can be used to choose a command from the menu or toolbar, take action if a command is chosen, set an insertion point (IP), or show selection feedback.

### -field ISG_DoubleTap:0x11

A double-click of the left mouse button. This can be used to select a word or open a file or folder.

### -field ISG_RightTap:0x12

A click of the right mouse button. This can be used to show a shortcut menu.

### -field ISG_Drag:0x13

A drag of the mouse while pressing the left mouse button. This can be used to drag-select (such as in Microsoft Word when starting with an IP), select multiple words, drag (such as when dragging an object in Microsoft Windows), or scroll.

### -field ISG_RightDrag:0x14

A press and hold followed by a stroke, which maps to a right drag of a mouse. This can be used to drag (such as when dragging an object or selection followed by a shortcut menu).

### -field ISG_HoldEnter:0x15

A press and hold of the left mouse button that lasts for a long time, which has no mouse equivalent. This is a fallback for when a user continues a press-and-hold action for a long time and the event reverts to a Tap.

### -field ISG_HoldLeave:0x16

Not implemented.

### -field ISG_HoverEnter:0x17

A pause of the mouse on an object. This can be used to show a ToolTip, roll-over effects, or other mouse pausing behaviors.

### -field ISG_HoverLeave:0x18

A mouse leaving a pause. This can be used to end ToolTip roll-over effects or other mouse pausing behaviors.

### -field ISG_Flick:0x1f

A flick gesture.

## -remarks

The flick gesture is recognized in Windows Vista and later versions of Windows.

The Windows Vista and Tablet PC operating systems support these gestures by default. When any of these gestures are recognized, the <a href="/windows/desktop/tablet/inkcollector-systemgesture">SystemGesture</a> event fires automatically. Many of these gestures map to traditional mouse events. For instance, the Tap system gesture mimics a click of the left mouse button.

A system gesture is separate from an application gesture. Application gestures are defined in the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture</a> enumeration type.

For more information about system gestures, see <a href="/windows/desktop/tablet/using-gestures">Using Gestures</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-gethotpoint">GetHotPoint Method</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>



<a href="/windows/desktop/tablet/inkpicture-systemgesture">SystemGesture Event [InkPicture Control]</a>



<a href="/windows/desktop/tablet/using-gestures">Using Gestures</a>
