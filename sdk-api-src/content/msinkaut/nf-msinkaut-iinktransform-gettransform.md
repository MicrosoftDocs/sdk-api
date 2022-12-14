---
UID: NF:msinkaut.IInkTransform.GetTransform
title: IInkTransform::GetTransform (msinkaut.h)
description: Gets the InkTransform member data.
helpviewer_keywords: ["GetTransform","GetTransform method [Tablet PC]","GetTransform method [Tablet PC]","IInkTransform interface","IInkTransform interface [Tablet PC]","GetTransform method","IInkTransform.GetTransform","IInkTransform::GetTransform","d6aec579-7fa4-4cfb-8f63-2810b0c40103","msinkaut/IInkTransform::GetTransform","tablet.inktransform_gettransform"]
old-location: tablet\inktransform_gettransform.htm
tech.root: tablet
ms.assetid: d6aec579-7fa4-4cfb-8f63-2810b0c40103
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [Tablet PC], GetTransform method [Tablet PC],IInkTransform interface, IInkTransform interface [Tablet PC],GetTransform method, IInkTransform.GetTransform, IInkTransform::GetTransform, d6aec579-7fa4-4cfb-8f63-2810b0c40103, msinkaut/IInkTransform::GetTransform, tablet.inktransform_gettransform
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkTransform::GetTransform
 - msinkaut/IInkTransform::GetTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTransform.GetTransform
---

# IInkTransform::GetTransform


## -description

Gets the <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> member data.

## -parameters

### -param eM11 [out]

 The real number that specifies the element in the first row, first column.

### -param eM12 [out]

 The real number that specifies the element in the first row, second column.

### -param eM21 [out]

 The real number that specifies the element in the second row, first column.

### -param eM22 [out]

 The real number that specifies the element in the second row, second column.

### -param eDx [out]

 The real number that specifies the element in the third row, first column.

### -param eDy [out]

 The real number that specifies the element in the third row, second column.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
</table>

## -remarks

An <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object represents a 33 matrix that, in turn, represents an affine transformation. The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).

## -see-also

<a href="../msinkaut/nn-msinkaut-iinktransform.md">IInkTransform</a>



<a href="/windows/desktop/tablet/inktransform-class">InkTransform Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform">SetTransform Method</a>
