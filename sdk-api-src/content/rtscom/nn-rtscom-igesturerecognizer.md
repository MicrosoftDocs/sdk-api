---
UID: NN:rtscom.IGestureRecognizer
title: IGestureRecognizer (rtscom.h)
description: Reacts to events by recognizing gestures and adding gesture data to the input queue.
old-location: tablet\igesturerecognizer.htm
tech.root: tablet
ms.assetid: dfdc00d6-c843-4298-9773-92775406fbf7
ms.date: 12/05/2018
ms.keywords: IGestureRecognizer, IGestureRecognizer interface [Tablet PC], IGestureRecognizer interface [Tablet PC],described, dfdc00d6-c843-4298-9773-92775406fbf7, rtscom/IGestureRecognizer, tablet.igesturerecognizer
f1_keywords:
- rtscom/IGestureRecognizer
dev_langs:
- c++
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RTSCom.dll
api_name:
- IGestureRecognizer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGestureRecognizer interface


## -description



Reacts to events by recognizing gestures and adding gesture data to the input queue.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGestureRecognizer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGestureRecognizer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-enablegestures">EnableGestures</a>
</td>
<td align="left" width="63%">
Sets a value that indicates to which application gestures the <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object responds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-reset">Reset</a>
</td>
<td align="left" width="63%">
Clears the <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object of past stroke information.

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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-get_enabled">Enabled</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-get_maxstrokecount">MaxStrokeCount</a>


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



This interface is implemented by the <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>.

The gesture recognizer analyzes digitizer input and injects gesture recognition results into the input queue.

Adding an instance of the <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> to multiple <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> instances is not a valid operation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>
 

 

