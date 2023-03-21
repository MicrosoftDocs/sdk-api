---
UID: NE:msinkaut.InkCollectionMode
title: InkCollectionMode (msinkaut.h)
description: Defines values that determine whether ink, gestures, or ink and gestures are recognized as the user writes.
helpviewer_keywords: ["41928d0a-e485-4542-860c-5ffd260d3cb8","ICM_GestureOnly","ICM_InkAndGesture","ICM_InkOnly","InkCollectionMode","InkCollectionMode enumeration [Tablet PC]","msinkaut/ICM_GestureOnly","msinkaut/ICM_InkAndGesture","msinkaut/ICM_InkOnly","msinkaut/InkCollectionMode","tablet.inkcollectionmode"]
old-location: tablet\inkcollectionmode.htm
tech.root: tablet
ms.assetid: 41928d0a-e485-4542-860c-5ffd260d3cb8
ms.date: 12/05/2018
ms.keywords: 41928d0a-e485-4542-860c-5ffd260d3cb8, ICM_GestureOnly, ICM_InkAndGesture, ICM_InkOnly, InkCollectionMode, InkCollectionMode enumeration [Tablet PC], msinkaut/ICM_GestureOnly, msinkaut/ICM_InkAndGesture, msinkaut/ICM_InkOnly, msinkaut/InkCollectionMode, tablet.inkcollectionmode
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
req.typenames: InkCollectionMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkCollectionMode
 - msinkaut/InkCollectionMode
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
 - InkCollectionMode
---

# InkCollectionMode enumeration


## -description

Defines values that determine whether ink, gestures, or ink and gestures are recognized as the user writes.

## -enum-fields

### -field ICM_InkOnly:0

Collects only ink, creating a stroke.

The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>FALSE</b>, meaning that gestures are not collected (all other event interests remain as they were).

### -field ICM_GestureOnly

Collects only gestures and does not create a stroke. Gestures can be either single or multi-stroke. Multi-stroke gestures are accepted if the strokes are made within the time set by the built-in timer of the recognizer.

All stroke-related and packet-related events do not fire from the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>. Cursor events do fire, and ink is always deleted.

The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>TRUE</b>, meaning that gestures are collected (all other event interests remain as they were).

### -field ICM_InkAndGesture

Accepts only single-stroke gestures. The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event fires first, giving the user the ability to say <i>Cancel</i> = <b>TRUE</b> or <b>FALSE</b>. The default is <b>TRUE</b>, except when <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">NoGesture</a> is the primary gesture, <i>Cancel</i> defaults to <b>FALSE</b>. If <b>TRUE</b>, the ink is a gesture and is deleted. If <b>FALSE</b>, the gesture is ink and a <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event fires.

The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests are kept as they were).

## -remarks

If a user attempts a right-click and moves the pen when in InkOnly or InkAndGesture mode, ink flows from the pen tip. When handling the <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event, you should erase the ink that flowed as a result of the pen movement.

When the <b>InkCollectionMode</b> is set to GestureOnly (set through the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> property), the timeout between when a user adds a gesture and when the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event occurs is a fixed value that cannot be altered programmatically. Gesture recognition is faster in InkAndGesture mode. To prevent the collection of ink while in InkAndGesture mode, you can:

<ul>
<li>Set <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> to InkAndGesture.</li>
<li>In the <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event, delete the stroke.</li>
<li>In the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event, process the gesture.</li>
<li>Set <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a> to <b>FALSE</b>.</li>
</ul>
When using this enumeration with the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control (or the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> objects) on a system that has the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) installed but that doesn't have recognizers, the mode cannot be set to GestureOnly or InkAndGesture.

The ink collector always creates either a stroke (InkOnly mode) or a gesture (GestureOnly mode) and sometimes created both (InkAndGesture mode).

Typical scenarios for each mode follow.

<ul>
<li>InkOnly:<ol>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a> event fires.</li>
<li>
<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object is created.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a> event fires.</li>
</ol>
<div class="alert"><b>Note</b>  You may not always want to fire the <a href="/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a> event. If you want to continue drawing ink, you may return to the <a href="/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> or <a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a> events after a stroke is completed.</div>
<div> </div>
</li>
<li>GestureOnly:<ol>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a> event fires.</li>
<li>Either an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture</a> object is created or, if the cursor movement does not represent a gesture, nothing happens.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a> event fires.</li>
</ol>
<div class="alert"><b>Note</b>  Either single or multi-stroke gestures are accepted in this mode.</div>
<div> </div>
</li>
<li>InkAndGesture:<ol>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a> event fires.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a> event fires.</li>
<li>Either an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture</a> object or an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object is created.</li>
<li>
<a href="/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a> event fires.</li>
</ol>
<div class="alert"><b>Note</b>  Only single-stroke gestures are accepted in this mode.</div>
<div> </div>
</li>
</ul>
Unwanted behavior might occur when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> property is set to InkAndGesture and the interest of an object or control in a known gesture is set (by calling the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus">SetGestureStatus</a> method). If a user draws ink that resembles a gesture that is in the recognizer's list of recognition alternates, the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event fires and ink disappears, even if the gesture is not the top alternate. To prevent the ink from disappearing and cancel collection of the gesture, set <i>Cancel</i> to <b>TRUE</b> if the event is one to which you do not want the recognizer to respond.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode Property [InkCollector Class]</a>



<a href="/windows/desktop/tablet/inkcollector-gesture">Gesture Event</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>



<a href="/windows/desktop/tablet/inkcollector-stroke">Stroke Event</a>
