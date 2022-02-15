---
UID: NN:msinkaut15.IInkDivisionResult
title: IInkDivisionResult (msinkaut15.h)
description: Represents the layout analysis of the collection of strokes contained by the InkDivider object.
helpviewer_keywords: ["IInkDivisionResult","IInkDivisionResult interface [Tablet PC]","IInkDivisionResult interface [Tablet PC]","described","d1a71976-2825-48d2-812c-fd2336cd4c1d","msinkaut15/IInkDivisionResult","tablet.iinkdivisionresult"]
old-location: tablet\iinkdivisionresult.htm
tech.root: tablet
ms.assetid: d1a71976-2825-48d2-812c-fd2336cd4c1d
ms.date: 12/05/2018
ms.keywords: IInkDivisionResult, IInkDivisionResult interface [Tablet PC], IInkDivisionResult interface [Tablet PC],described, d1a71976-2825-48d2-812c-fd2336cd4c1d, msinkaut15/IInkDivisionResult, tablet.iinkdivisionresult
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDivisionResult
 - msinkaut15/IInkDivisionResult
dev_langs:
 - c++
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
---

# IInkDivisionResult interface


## -description

Represents the layout analysis of the collection of strokes contained by the <a href="/windows/desktop/tablet/inkdivider-class">InkDivider</a> object.

## -inheritance

The <b>IInkDivisionResult</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivisionResult</b> also has these types of members:

## -remarks

The <b>IInkDivisionResult</b> object is the result of calling the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-divide">Divide</a> method of the <a href="/windows/desktop/tablet/inkdivider-class">InkDivider</a> object. Each <b>IInkDivisionResult</b> represents a snapshot of the layout analysis of the collection of strokes contained by the <b>InkDivider</b>.

The analysis results can be divided into a collection of structural units by calling the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType</a> method.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits Interface</a>



<a href="/windows/desktop/tablet/inkdivider-class">InkDivider Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType Method</a>
