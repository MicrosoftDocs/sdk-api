---
UID: NN:msinkaut.IInkGesture
title: IInkGesture (msinkaut.h)
description: Represents the ability to query particular properties of a gesture returned from a gesture recognition.
helpviewer_keywords: ["87a1db34-371e-4c02-a470-55f35dfbf4ab","IInkGesture","IInkGesture interface [Tablet PC]","IInkGesture interface [Tablet PC]","described","msinkaut/IInkGesture","tablet.iinkgesture"]
old-location: tablet\iinkgesture.htm
tech.root: tablet
ms.assetid: 87a1db34-371e-4c02-a470-55f35dfbf4ab
ms.date: 12/05/2018
ms.keywords: 87a1db34-371e-4c02-a470-55f35dfbf4ab, IInkGesture, IInkGesture interface [Tablet PC], IInkGesture interface [Tablet PC],described, msinkaut/IInkGesture, tablet.iinkgesture
f1_keywords:
- msinkaut/IInkGesture
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
- IInkGesture
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkGesture interface


## -description



Represents the ability to query particular properties of a gesture returned from a gesture recognition.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkGesture</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkGesture</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkGesture</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-gethotpoint">GetHotPoint</a>
</td>
<td align="left" width="63%">
Retrieves the hot point of the gesture in ink space coordinates.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkGesture</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence">Confidence</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in a gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_id">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the value of the application gesture.

</td>
</tr>
</table> 


## -remarks



Gesture support is built-in by using the Microsoft gesture recognizer. Available gestures are found in the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture</a> enumeration type. For more information about gestures, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-gestures">Using Gestures</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ms702526(v=vs.85)">Command Input on the Tablet PC</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture">InkSystemGesture Enumeration</a>
 

 

