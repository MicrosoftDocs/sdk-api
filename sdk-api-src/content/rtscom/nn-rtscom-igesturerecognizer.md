---
UID: NN:rtscom.IGestureRecognizer
title: IGestureRecognizer
author: windows-driver-content
description: Reacts to events by recognizing gestures and adding gesture data to the input queue.
old-location: tablet\igesturerecognizer.htm
old-project: tablet
ms.assetid: dfdc00d6-c843-4298-9773-92775406fbf7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IGestureRecognizer, IGestureRecognizer interface [Tablet PC], IGestureRecognizer interface [Tablet PC], described, dfdc00d6-c843-4298-9773-92775406fbf7, rtscom/IGestureRecognizer, tablet.igesturerecognizer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rtscom.h
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IGestureRecognizer
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IGestureRecognizer interface


## -description



Reacts to events by recognizing gestures and adding gesture data to the input queue.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGestureRecognizer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGestureRecognizer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGestureRecognizer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59d39c2c-1c92-4325-b534-36b97a7df20f">EnableGestures</a>
</td>
<td align="left" width="63%">
Sets a value that indicates to which application gestures the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> object responds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Clears the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> object of past stroke information.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGestureRecognizer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether gesture recognition is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d7f40294-437a-4d5c-9389-1798102d0d8f">MaxStrokeCount</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the maximum number of strokes allowed per gesture recognition.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>.

The gesture recognizer analyzes digitizer input and injects gesture recognition results into the input queue.

Adding an instance of the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> to multiple <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> instances is not a valid operation.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>
 

 

