---
UID: NF:msinkaut.IInkTransform.Rotate
title: IInkTransform::Rotate (msinkaut.h)
description: Changes the amount, measured in degrees, to change the rotation factor of the InkTransform object and optionally the center point of the rotation.
helpviewer_keywords: ["17d7e4b0-ccde-4ad9-9bdc-0f6a72ee762e","IInkTransform interface [Tablet PC]","Rotate method","IInkTransform.Rotate","IInkTransform::Rotate","Rotate","Rotate method [Tablet PC]","Rotate method [Tablet PC]","IInkTransform interface","msinkaut/IInkTransform::Rotate","tablet.inktransform_rotate"]
old-location: tablet\inktransform_rotate.htm
tech.root: tablet
ms.assetid: 17d7e4b0-ccde-4ad9-9bdc-0f6a72ee762e
ms.date: 12/05/2018
ms.keywords: 17d7e4b0-ccde-4ad9-9bdc-0f6a72ee762e, IInkTransform interface [Tablet PC],Rotate method, IInkTransform.Rotate, IInkTransform::Rotate, Rotate, Rotate method [Tablet PC], Rotate method [Tablet PC],IInkTransform interface, msinkaut/IInkTransform::Rotate, tablet.inktransform_rotate
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
 - IInkTransform::Rotate
 - msinkaut/IInkTransform::Rotate
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
 - IInkTransform.Rotate
---

# IInkTransform::Rotate


## -description

Changes the amount, measured in degrees, to change the rotation factor of the <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object and optionally the center point of the rotation.

## -parameters

### -param Degrees [in]

The degrees by which to rotate clockwise. Without the optional x and y arguments, rotation takes place around the origin point, which by default is the upper left corner of the ink collection area to which the transform is applied.

### -param x [in, optional]

Optional. The x-coordinate of the point in ink space coordinates around which rotation occurs. The default value is 0.

### -param y [in, optional]

Optional. The y-coordinate of the point in ink space coordinates around which rotation occurs. The default value is 0.

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
</table>

## -remarks

The center point defaults to the origin.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinktransform.md">IInkTransform</a>



<a href="/windows/desktop/tablet/inktransform-class">InkTransform Class</a>
