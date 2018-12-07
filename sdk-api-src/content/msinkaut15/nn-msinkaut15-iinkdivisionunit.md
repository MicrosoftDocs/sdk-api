---
UID: NN:msinkaut15.IInkDivisionUnit
title: IInkDivisionUnit
author: windows-sdk-content
description: Represents a single structural element within an IInkDivisionResult object.
old-location: tablet\iinkdivisionunit.htm
tech.root: tablet
ms.assetid: 5c5479e0-7568-40c8-bb75-e2ded3ac86b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5c5479e0-7568-40c8-bb75-e2ded3ac86b7, IInkDivisionUnit, IInkDivisionUnit interface [Tablet PC], IInkDivisionUnit interface [Tablet PC],described, msinkaut15/IInkDivisionUnit, tablet.iinkdivisionunit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDivisionUnit interface


## -description



Represents a single structural element within an <a href="https://msdn.microsoft.com/d1a71976-2825-48d2-812c-fd2336cd4c1d">IInkDivisionResult</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionUnit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkDivisionUnit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDivisionUnit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/702ec977-2d87-4d52-916e-423f1df03829">ToString</a>
</td>
<td align="left" width="63%">
Has the default recognizer perform recognition on the collection of strokes and returns the top string of the top alternate of the recognition result.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionUnit</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c1aaaa62-34fc-4cd4-bd68-47f828bb59b1">DivisionType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the type of the element as an <a href="https://msdn.microsoft.com/00e1188e-58c0-4681-ad04-e53079d478fd">InkDivisionType</a> enumeration value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c56bf393-7630-4399-894e-34b41b068370">RecognitionString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the recognition text of the element, or <b>NULL</b> for drawing elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c1c0b5e-2f39-4901-a8c7-96dd65ced5c8">RotationTransform</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the transformation matrix for a segment or line element that rotates the strokes for the element to horizontal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/505df3d7-740e-46fc-a942-2820b3428564">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that corresponds to this element.

</td>
</tr>
</table> 


## -remarks



Use the <a href="https://msdn.microsoft.com/332a9365-526e-43df-841f-20eed07762e7">Item</a> method to return a single element from a <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">DivisionUnits</a> collection.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits Interface</a>



<a href="https://msdn.microsoft.com/00e1188e-58c0-4681-ad04-e53079d478fd">InkDivisionType Enumeration</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

