---
UID: NN:msinkaut15.IInkDivisionUnit
title: IInkDivisionUnit (msinkaut15.h)
description: Represents a single structural element within an IInkDivisionResult object.
helpviewer_keywords: ["5c5479e0-7568-40c8-bb75-e2ded3ac86b7","IInkDivisionUnit","IInkDivisionUnit interface [Tablet PC]","IInkDivisionUnit interface [Tablet PC]","described","msinkaut15/IInkDivisionUnit","tablet.iinkdivisionunit"]
old-location: tablet\iinkdivisionunit.htm
tech.root: tablet
ms.assetid: 5c5479e0-7568-40c8-bb75-e2ded3ac86b7
ms.date: 12/05/2018
ms.keywords: 5c5479e0-7568-40c8-bb75-e2ded3ac86b7, IInkDivisionUnit, IInkDivisionUnit interface [Tablet PC], IInkDivisionUnit interface [Tablet PC],described, msinkaut15/IInkDivisionUnit, tablet.iinkdivisionunit
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
 - IInkDivisionUnit
 - msinkaut15/IInkDivisionUnit
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
 - IInkDivisionUnit
---

# IInkDivisionUnit interface


## -description

Represents a single structural element within an <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object.

## -inheritance

The <b>IInkDivisionUnit</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivisionUnit</b> also has these types of members:

## -remarks

Use the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunits-item">Item</a> method to return a single element from a <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">DivisionUnits</a> collection.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits Interface</a>



<a href="/windows/desktop/api/msinkaut15/ne-msinkaut15-inkdivisiontype">InkDivisionType Enumeration</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
