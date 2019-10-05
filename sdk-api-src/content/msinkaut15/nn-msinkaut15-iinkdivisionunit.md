---
UID: NN:msinkaut15.IInkDivisionUnit
title: IInkDivisionUnit (msinkaut15.h)
author: windows-sdk-content
description: Represents a single structural element within an IInkDivisionResult object.
old-location: tablet\iinkdivisionunit.htm
tech.root: tablet
ms.assetid: 5c5479e0-7568-40c8-bb75-e2ded3ac86b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5c5479e0-7568-40c8-bb75-e2ded3ac86b7, IInkDivisionUnit, IInkDivisionUnit interface [Tablet PC], IInkDivisionUnit interface [Tablet PC],described, msinkaut15/IInkDivisionUnit, tablet.iinkdivisionunit
ms.topic: interface
f1_keywords: 
 - "msinkaut15/IInkDivisionUnit"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDivisionUnit interface


## -description



Represents a single structural element within an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionUnit</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivisionUnit</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms699557(v=vs.85)">ToString</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype">DivisionType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the type of the element as an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/ne-msinkaut15-inkdivisiontype">InkDivisionType</a> enumeration value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)">RecognitionString</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform">RotationTransform</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that corresponds to this element.

</td>
</tr>
</table> 


## -remarks



Use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunits-item">Item</a> method to return a single element from a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">DivisionUnits</a> collection.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/ne-msinkaut15-inkdivisiontype">InkDivisionType Enumeration</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
 

 

