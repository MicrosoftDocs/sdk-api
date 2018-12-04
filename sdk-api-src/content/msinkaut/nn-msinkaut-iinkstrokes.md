---
UID: NN:msinkaut.IInkStrokes
title: IInkStrokes
author: windows-sdk-content
description: "."
old-location: tablet\iinkstrokes.htm
tech.root: tablet
ms.assetid: 496234C1-C20B-46FE-A9BB-4B90C14FEB46
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IInkStrokes, IInkStrokes interface [Tablet PC], IInkStrokes interface [Tablet PC],described, msinkaut/IInkStrokes, tablet.iinkstrokes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkStrokes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokes interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkStrokes</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkStrokes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkStrokes</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d32dcaef-3beb-4ee1-84d6-5944278936f6">StrokesAdded</a>
</td>
<td align="left" width="63%">
Occurs when one or more strokes are added to the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58d78143-c733-45dc-ae5f-fe13136010db">StrokesRemoved</a>
</td>
<td align="left" width="63%">
Occurs when one or more strokes are deleted from the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkStrokes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ea0932a-ba21-4c6a-a3bc-c122b5805e86">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to an existing InkStrokes collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76580828-c776-4787-843c-db0acb768321">AddStrokes</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">Strokes</a> collection to an existing Strokes collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef434bcc-610c-449d-90d4-b3f897408f34">Clip</a>
</td>
<td align="left" width="63%">
Removes portions of an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that are outside a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33641615-c2dc-43ee-b7be-8f24c38bac6b">GetBoundingBox</a>
</td>
<td align="left" width="63%">
Gets the bounding box in ink space coordinates for either all of the strokes in an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, an individual stroke, or an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecffbdf0-4b1c-46de-bc4c-c44812dae27a">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object at the specified index within the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b249edd9-dfa4-4538-9764-a4365f9df527">ModifyDrawingAttributes</a>
</td>
<td align="left" width="63%">
Sets the drawing attributes of all of the strokes in an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4754a211-b90c-453a-91b2-9f49ad31621d">Move</a>
</td>
<td align="left" width="63%">
Applies a translation to the ink of an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce7a7842-c7c8-4f73-8f68-05b22c2199de">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object from a <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a1a2027-e0b7-40c5-b396-b6b4039d6b5b">RemoveRecognitionResult</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/5d6e7147-b312-4989-8d8f-88cb2221f6f0">RecognitionResult</a> that is associated with the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f90d175-747c-4bf5-978a-286b69bf068a">RemoveStrokes</a>
</td>
<td align="left" width="63%">
Removes strokes from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d198215d-9504-4c87-addb-63d863a6ede3">Rotate</a>
</td>
<td align="left" width="63%">
Rotates the ink using an angle in degrees around a center point of the rotation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/592b28e7-2bde-497d-8a15-2a1b4cc509b1">ScaleToRectangle</a>
</td>
<td align="left" width="63%">
Scales the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to fit in the specified <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7b69554-69e3-4a45-9313-16a3529863e9">ScaleTransform</a>
</td>
<td align="left" width="63%">
Applies the specified horizontal and vertical factors to the transform or ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ae8cf5a-b113-46e8-b8c2-6605f017f826">Shear</a>
</td>
<td align="left" width="63%">
Shears the ink in the stroke or strokes by the specified horizontal and vertical factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f1d68b-16c2-4d97-ae5f-091e5ec285c2">ToString</a>
</td>
<td align="left" width="63%">

<a href="https://msdn.microsoft.com/e1f1d68b-16c2-4d97-ae5f-091e5ec285c2">ToString</a> is no longer available for use as of Windows Vista.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/910ae16d-be9a-422c-b9af-9a2df28df463">Transform</a>
</td>
<td align="left" width="63%">
Applies a linear transformation to an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection, which can represent scaling, rotation, translation, and combinations of transformations.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkStrokes</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0148627-11fc-47ee-8b77-1aa5700343cb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of objects or collections contained in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/973d9aaa-0897-4e3f-a57f-ce505853f310">Ink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that contains a collection of strokes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5d6e7147-b312-4989-8d8f-88cb2221f6f0">RecognitionResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult</a> object of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
</table> 

