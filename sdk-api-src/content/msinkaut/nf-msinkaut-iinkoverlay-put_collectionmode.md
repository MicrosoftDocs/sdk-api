---
UID: NF:msinkaut.IInkOverlay.put_CollectionMode
title: IInkOverlay::put_CollectionMode
author: windows-sdk-content
description: Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes.
old-location: tablet\inkoverlay_collectionmode.htm
tech.root: tablet
ms.assetid: 3538213f-b9c3-474c-a847-40915c8961dd
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: CollectionMode property [Tablet PC], CollectionMode property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],CollectionMode property, IInkOverlay.CollectionMode, IInkOverlay.put_CollectionMode, IInkOverlay::CollectionMode, IInkOverlay::get_CollectionMode, IInkOverlay::put_CollectionMode, InkOverlay.get_CollectionMode, InkOverlay.put_CollectionMode, msinkaut/IInkOverlay::CollectionMode, msinkaut/IInkOverlay::get_CollectionMode, msinkaut/IInkOverlay::put_CollectionMode, put_CollectionMode, tablet.inkoverlay_collectionmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IInkOverlay.CollectionMode
 - IInkOverlay.get_CollectionMode
 - IInkOverlay.put_CollectionMode
 - InkOverlay.get_CollectionMode
 - InkOverlay.put_CollectionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkOverlay::put_CollectionMode


## -description



Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes.



This property is read/write.


## -parameters


## -remarks



For a list of the modes that you can use, see the <a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">InkCollectionMode</a> enumeration type. However, when using the <a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a> property on a system that has the Microsoft Windows? XP Tablet PC Edition Software Development Kit (SDK) installed but that doesn't have recognizer installed, the mode cannot be set to <b>GestureOnly</b> or <b>InkAndGesture</b>.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, or the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control generates an error if you try to change the <a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a> property while ink is being collected. To avoid this conflict, check the <a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk</a> property before changing the <b>CollectionMode</b> property.</div>
<div> </div>
The following behaviors occur for each of the <a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a> values:


<a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">InkOnly</a> mode

<ul>
<li>Only ink is collected; gestures are not.</li>
<li>The <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event interest is set to <b>FALSE</b> (all other event interests remain as they were).</li>
</ul>

<a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">GestureOnly</a> mode

<ul>
<li>Only gestures are collected; ink is not. The strokes are deleted after they are sent to the gesture recognizer.</li>
<li>The <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests remain as they were).</li>
<li>The ink collector does not fire the following stroke and packet related events: the <a href="https://msdn.microsoft.com/bf914849-ef33-4746-b2e1-c768cd1d87aa">CursorDown</a>, <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a>, <a href="https://msdn.microsoft.com/2682e7ba-dabd-497e-aea4-6d3f837f4f10">NewPackets</a>, and <a href="https://msdn.microsoft.com/e8eacdec-0381-435f-b453-24dca1c507c9">NewInAirPackets</a> events.</li>
<li>Cursor events fire.</li>
<li>Ink is always deleted.</li>
</ul>

<a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">InkAndGesture</a> mode

<ul>
<li>Both ink and gestures are collected.</li>
<li>Only single-stroke gestures are recognized.</li>
<li>The <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event interest is set to <b>TRUE</b> (all other event interests remain as they were).</li>
<li>The <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event fires first, allowing you to accept or cancel the gesture. To cancel the gesture, set the <i>Cancel</i> parameter to <b>TRUE</b>. Canceling the gesture forces the ink collector to collect the ink.</li>
</ul>
Changing the collection mode does not alter the status of individual gestures.

Unwanted behavior might occur when <a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a> is set to <a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">InkAndGesture</a> and an object's/control's interest in a known gesture is set (by calling the <a href="https://msdn.microsoft.com/7bab227f-d095-48e8-856f-6446e62826dd">SetGestureStatus</a> method). If you draw ink that looks something like the known gesture and the known gesture is in the recognizer's list of alternates, the <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event fires and ink disappears, even if the gesture is not the top alternate. To prevent the ink from disappearing and cancel collection of the gesture, set the <i>Cancel</i> parameter to <b>TRUE</b> if the event is one that you have no interest in.

When <a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a> is set to <a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">GestureOnly</a>, the timeout between when a user adds a gesture and when the <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event occurs is a fixed value that cannot be altered programmatically. Gesture recognition is faster in <b>InkAndGesture</b> mode. To prevent the collection of ink while in <b>InkAndGesture</b> mode, you can:

<ol>
<li>Set the <a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a> property to <b>InkAndGesture</b>.</li>
<li>In the <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a> event, delete the stroke.</li>
<li>In the <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event, process the gesture.</li>
<li>Set <a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering</a> to <b>FALSE</b> to prevent the flow of ink while gesturing.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk Property</a>



<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="https://msdn.microsoft.com/ACE11946-113B-42EE-A3F1-0036B1DF8141">IInkOverlay</a>



<a href="https://msdn.microsoft.com/41928d0a-e485-4542-860c-5ffd260d3cb8">InkCollectionMode Enumeration</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>
 

 

