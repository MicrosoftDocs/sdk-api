---
UID: NN:msinkaut15.IInkDivider
title: IInkDivider (msinkaut15.h)
description: .
helpviewer_keywords: ["IInkDivider","IInkDivider interface [Tablet PC]","IInkDivider interface [Tablet PC]","described","msinkaut15/IInkDivider","tablet.iinkdivider"]
old-location: tablet\iinkdivider.htm
tech.root: tablet
ms.assetid: 6DF54C8E-1E0D-4F9D-A6E4-AFE0E8894BE9
ms.date: 12/05/2018
ms.keywords: IInkDivider, IInkDivider interface [Tablet PC], IInkDivider interface [Tablet PC],described, msinkaut15/IInkDivider, tablet.iinkdivider
f1_keywords:
- msinkaut15/IInkDivider
dev_langs:
- c++
req.header: msinkaut15.h
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
- msinkaut15.h
api_name:
- IInkDivider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDivider interface


## -description

Represents the ability to analyze the layout of a collection of ink strokes and divide them into text and graphics.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDivider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-divide">Divide</a>
</td>
<td align="left" width="63%">
Returns a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object that contains the results of the layout analysis of strokes in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDivider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight">LineHeight</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the expected handwriting height, in HIMETRIC units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext">RecognizerContext</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object that the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object uses for layout analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection on which the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object performs layout analysis.

</td>
</tr>
</table> 

