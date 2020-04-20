---
UID: NF:msinkaut.IInkCollector.get_CollectionMode
title: IInkCollector::get_CollectionMode (msinkaut.h)
description: Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes.helpviewer_keywords: ["390fa1a1-254a-4070-806c-c8c478f69254","CollectionMode property [Tablet PC]","CollectionMode property [Tablet PC]","IInkCollector interface","IInkCollector interface [Tablet PC]","CollectionMode property","IInkCollector.CollectionMode","IInkCollector.get_CollectionMode","IInkCollector.put_CollectionMode","IInkCollector::CollectionMode","IInkCollector::get_CollectionMode","IInkCollector::put_CollectionMode","InkCollector.get_CollectionMode","InkCollector.put_CollectionMode","get_CollectionMode","msinkaut/IInkCollector::CollectionMode","msinkaut/IInkCollector::get_CollectionMode","msinkaut/IInkCollector::put_CollectionMode","put_CollectionMode","tablet.inkcollector_collectionmode"]
old-location: tablet\inkcollector_collectionmode.htm
tech.root: tablet
ms.assetid: 390fa1a1-254a-4070-806c-c8c478f69254
ms.date: 12/05/2018
ms.keywords: 390fa1a1-254a-4070-806c-c8c478f69254, CollectionMode property [Tablet PC], CollectionMode property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],CollectionMode property, IInkCollector.CollectionMode, IInkCollector.get_CollectionMode, IInkCollector.put_CollectionMode, IInkCollector::CollectionMode, IInkCollector::get_CollectionMode, IInkCollector::put_CollectionMode, InkCollector.get_CollectionMode, InkCollector.put_CollectionMode, get_CollectionMode, msinkaut/IInkCollector::CollectionMode, msinkaut/IInkCollector::get_CollectionMode, msinkaut/IInkCollector::put_CollectionMode, put_CollectionMode, tablet.inkcollector_collectionmode
f1_keywords:
- msinkaut/IInkCollector.CollectionMode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkCollector.CollectionMode
- IInkCollector.get_CollectionMode
- IInkCollector.put_CollectionMode
- put_CollectionMode
- IInkCollector.put_CollectionMode
- InkCollector.get_CollectionMode
- InkCollector.put_CollectionMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCollector::get_CollectionMode


## -description



Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes.



This property is read/write.


## -parameters


## -remarks



For a list of the modes that you can use, see the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkCollectionMode</a> enumeration type. However, when using the <b>CollectionMode</b> property on a system that has the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) installed but that doesn't have recognizer installed, the mode cannot be set to <b>GestureOnly</b> or <b>InkAndGesture</b>.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control generates an error if you try to change the <b>CollectionMode</b> property while ink is being collected. To avoid this conflict, check the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a> property before changing the <b>CollectionMode</b> property.</div>
<div> </div>
The following behaviors occur for each of the <b>CollectionMode</b> values:


<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkOnly</a> mode

<ul>
<li>Only ink is collected; gestures are not.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>FALSE</b> (all other event interests remain as they were).</li>
</ul>

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">GestureOnly</a> mode

<ul>
<li>Only gestures are collected; ink is not. The strokes are deleted after they are sent to the gesture recognizer.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests remain as they were).</li>
<li>The ink collector does not fire the following stroke and packet related events: the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-stroke">Stroke</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a>, and <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> events.</li>
<li>Cursor events fire.</li>
<li>Ink is always deleted.</li>
</ul>

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkAndGesture</a> mode

<ul>
<li>Both ink and gestures are collected.</li>
<li>Only single-stroke gestures are recognized.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests remain as they were).</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event fires first, allowing you to accept or cancel the gesture. To cancel the gesture, set the <i>Cancel</i> parameter to <b>TRUE</b>. Canceling the gesture forces the ink collector to collect the ink.</li>
</ul>
Changing the collection mode does not alter the status of individual gestures.

Unwanted behavior might occur when <b>CollectionMode</b> is set to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkAndGesture</a> and an object's/control's interest in a known gesture is set (by calling the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus">SetGestureStatus</a> method). If you draw ink that looks something like the known gesture and the known gesture is in the recognizer's list of alternates, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event fires and ink disappears, even if the gesture is not the top alternate. To prevent the ink from disappearing and cancel collection of the gesture, set the <i>Cancel</i> parameter to <b>TRUE</b> if the event is one that you have no interest in.

When <b>CollectionMode</b> is set to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">GestureOnly</a>, the timeout between when a user adds a gesture and when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event occurs is a fixed value that cannot be altered programmatically. Gesture recognition is faster in <b>InkAndGesture</b> mode. To prevent the collection of ink while in <b>InkAndGesture</b> mode, you can:

<ol>
<li>Set the <b>CollectionMode</b> property to <b>InkAndGesture</b>.</li>
<li>In the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event, delete the stroke.</li>
<li>In the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event, process the gesture.</li>
<li>Set <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a> to <b>FALSE</b> to prevent the flow of ink while gesturing.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846796(v=VS.85).aspx">IInkCollector</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode">InkCollectionMode Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>
 

 

