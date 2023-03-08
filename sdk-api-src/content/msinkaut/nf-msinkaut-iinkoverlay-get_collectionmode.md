---
UID: NF:msinkaut.IInkOverlay.get_CollectionMode
title: IInkOverlay::get_CollectionMode (msinkaut.h)
description: Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes. (IInkOverlay.get_CollectionMode)
helpviewer_keywords: ["CollectionMode property [Tablet PC]","CollectionMode property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","CollectionMode property","IInkOverlay.CollectionMode","IInkOverlay.get_CollectionMode","IInkOverlay::CollectionMode","IInkOverlay::get_CollectionMode","IInkOverlay::put_CollectionMode","InkOverlay.get_CollectionMode","InkOverlay.put_CollectionMode","get_CollectionMode","msinkaut/IInkOverlay::CollectionMode","msinkaut/IInkOverlay::get_CollectionMode","msinkaut/IInkOverlay::put_CollectionMode","tablet.inkoverlay_collectionmode"]
old-location: tablet\inkoverlay_collectionmode.htm
tech.root: tablet
ms.assetid: 3538213f-b9c3-474c-a847-40915c8961dd
ms.date: 12/05/2018
ms.keywords: CollectionMode property [Tablet PC], CollectionMode property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],CollectionMode property, IInkOverlay.CollectionMode, IInkOverlay.get_CollectionMode, IInkOverlay::CollectionMode, IInkOverlay::get_CollectionMode, IInkOverlay::put_CollectionMode, InkOverlay.get_CollectionMode, InkOverlay.put_CollectionMode, get_CollectionMode, msinkaut/IInkOverlay::CollectionMode, msinkaut/IInkOverlay::get_CollectionMode, msinkaut/IInkOverlay::put_CollectionMode, tablet.inkoverlay_collectionmode
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkOverlay::get_CollectionMode
 - msinkaut/IInkOverlay::get_CollectionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.CollectionMode
 - IInkOverlay.get_CollectionMode
 - IInkOverlay.put_CollectionMode
 - InkOverlay.get_CollectionMode
 - InkOverlay.put_CollectionMode
---

# IInkOverlay::get_CollectionMode


## -description

Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes.



This property is read/write.

## -parameters

## -remarks

For a list of the modes that you can use, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkCollectionMode</a> enumeration type. However, when using the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> property on a system that has the Microsoft Windows? XP Tablet PC Edition Software Development Kit (SDK) installed but that doesn't have recognizer installed, the mode cannot be set to <b>GestureOnly</b> or <b>InkAndGesture</b>.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control generates an error if you try to change the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> property while ink is being collected. To avoid this conflict, check the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a> property before changing the <b>CollectionMode</b> property.</div>
<div> </div>
The following behaviors occur for each of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> values:


<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkOnly</a> mode

<ul>
<li>Only ink is collected; gestures are not.</li>
<li>The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>FALSE</b> (all other event interests remain as they were).</li>
</ul>

<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">GestureOnly</a> mode

<ul>
<li>Only gestures are collected; ink is not. The strokes are deleted after they are sent to the gesture recognizer.</li>
<li>The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests remain as they were).</li>
<li>The ink collector does not fire the following stroke and packet related events: the <a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a>, <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a>, <a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a>, and <a href="/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> events.</li>
<li>Cursor events fire.</li>
<li>Ink is always deleted.</li>
</ul>

<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkAndGesture</a> mode

<ul>
<li>Both ink and gestures are collected.</li>
<li>Only single-stroke gestures are recognized.</li>
<li>The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests remain as they were).</li>
<li>The <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event fires first, allowing you to accept or cancel the gesture. To cancel the gesture, set the <i>Cancel</i> parameter to <b>TRUE</b>. Canceling the gesture forces the ink collector to collect the ink.</li>
</ul>
Changing the collection mode does not alter the status of individual gestures.

Unwanted behavior might occur when <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> is set to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkAndGesture</a> and an object's/control's interest in a known gesture is set (by calling the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus">SetGestureStatus</a> method). If you draw ink that looks something like the known gesture and the known gesture is in the recognizer's list of alternates, the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event fires and ink disappears, even if the gesture is not the top alternate. To prevent the ink from disappearing and cancel collection of the gesture, set the <i>Cancel</i> parameter to <b>TRUE</b> if the event is one that you have no interest in.

When <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> is set to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">GestureOnly</a>, the timeout between when a user adds a gesture and when the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event occurs is a fixed value that cannot be altered programmatically. Gesture recognition is faster in <b>InkAndGesture</b> mode. To prevent the collection of ink while in <b>InkAndGesture</b> mode, you can:

<ol>
<li>Set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a> property to <b>InkAndGesture</b>.</li>
<li>In the <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event, delete the stroke.</li>
<li>In the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event, process the gesture.</li>
<li>Set <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a> to <b>FALSE</b> to prevent the flow of ink while gesturing.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkCollectionMode Enumeration</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
