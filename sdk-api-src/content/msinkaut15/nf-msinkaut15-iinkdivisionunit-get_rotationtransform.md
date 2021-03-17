---
UID: NF:msinkaut15.IInkDivisionUnit.get_RotationTransform
title: IInkDivisionUnit::get_RotationTransform (msinkaut15.h)
description: Gets the transformation matrix that the IInkDivisionUnit object uses to rotate the strokes to horizontal.
helpviewer_keywords: ["2c1c0b5e-2f39-4901-a8c7-96dd65ced5c8","IInkDivisionUnit interface [Tablet PC]","RotationTransform property","IInkDivisionUnit.RotationTransform","IInkDivisionUnit.get_RotationTransform","IInkDivisionUnit::RotationTransform","IInkDivisionUnit::get_RotationTransform","RotationTransform property [Tablet PC]","RotationTransform property [Tablet PC]","IInkDivisionUnit interface","get_RotationTransform","msinkaut15/IInkDivisionUnit::RotationTransform","msinkaut15/IInkDivisionUnit::get_RotationTransform","tablet.iinkdivisionunit_rotationtransform"]
old-location: tablet\iinkdivisionunit_rotationtransform.htm
tech.root: tablet
ms.assetid: 2c1c0b5e-2f39-4901-a8c7-96dd65ced5c8
ms.date: 12/05/2018
ms.keywords: 2c1c0b5e-2f39-4901-a8c7-96dd65ced5c8, IInkDivisionUnit interface [Tablet PC],RotationTransform property, IInkDivisionUnit.RotationTransform, IInkDivisionUnit.get_RotationTransform, IInkDivisionUnit::RotationTransform, IInkDivisionUnit::get_RotationTransform, RotationTransform property [Tablet PC], RotationTransform property [Tablet PC],IInkDivisionUnit interface, get_RotationTransform, msinkaut15/IInkDivisionUnit::RotationTransform, msinkaut15/IInkDivisionUnit::get_RotationTransform, tablet.iinkdivisionunit_rotationtransform
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
 - IInkDivisionUnit::get_RotationTransform
 - msinkaut15/IInkDivisionUnit::get_RotationTransform
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
 - IInkDivisionUnit.RotationTransform
 - IInkDivisionUnit.get_RotationTransform
 - IInkDivisionUnit.get_RotationTransform
---

# IInkDivisionUnit::get_RotationTransform


## -description

Gets the transformation matrix that the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object uses to rotate the strokes to horizontal.



This property is read-only.

## -parameters

## -remarks

Text recognizers
           perform best with horizontal handwriting. Apply this transformation to the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes</a> property of the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object before passing the strokes to an <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

<div class="alert"><b>Note</b>  For an <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object which represents a paragraph or drawing, this property returns <b>NULL</b>.</div>
<div> </div>
Use this property to level handwriting or to accurately draw lines or shapes around angled handwriting.

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit Interface</a>



<a href="/windows/desktop/tablet/inktransform-class">InkTransform Class</a>