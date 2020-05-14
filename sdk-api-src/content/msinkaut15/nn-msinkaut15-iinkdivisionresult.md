---
UID: NN:msinkaut15.IInkDivisionResult
title: IInkDivisionResult (msinkaut15.h)
description: Represents the layout analysis of the collection of strokes contained by the InkDivider object.helpviewer_keywords: ["IInkDivisionResult","IInkDivisionResult interface [Tablet PC]","IInkDivisionResult interface [Tablet PC]","described","d1a71976-2825-48d2-812c-fd2336cd4c1d","msinkaut15/IInkDivisionResult","tablet.iinkdivisionresult"]
old-location: tablet\iinkdivisionresult.htm
tech.root: tablet
ms.assetid: d1a71976-2825-48d2-812c-fd2336cd4c1d
ms.date: 12/05/2018
ms.keywords: IInkDivisionResult, IInkDivisionResult interface [Tablet PC], IInkDivisionResult interface [Tablet PC],described, d1a71976-2825-48d2-812c-fd2336cd4c1d, msinkaut15/IInkDivisionResult, tablet.iinkdivisionresult
f1_keywords:
- msinkaut15/IInkDivisionResult
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
- IInkDivisionResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDivisionResult interface


## -description



Represents the layout analysis of the collection of strokes contained by the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionResult</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivisionResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDivisionResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection that represents the requested structural units within the analysis result.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivisionResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that was used to create the analysis results.

</td>
</tr>
</table> 


## -remarks



The <b>IInkDivisionResult</b> object is the result of calling the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-divide">Divide</a> method of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object. Each <b>IInkDivisionResult</b> represents a snapshot of the layout analysis of the collection of strokes contained by the <b>InkDivider</b>.

The analysis results can be divided into a collection of structural units by calling the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType</a> method.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType Method</a>
 

 

