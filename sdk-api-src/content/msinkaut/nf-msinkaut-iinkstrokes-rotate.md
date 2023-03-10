---
UID: NF:msinkaut.IInkStrokes.Rotate
title: IInkStrokes::Rotate (msinkaut.h)
description: Rotates the ink using an angle in degrees around a center point of the rotation. (IInkStrokes.Rotate)
helpviewer_keywords: ["3b3d5a58-31e8-4d0e-a1c9-25bb36bb8d9c","IInkStrokes interface [Tablet PC]","Rotate method","IInkStrokes.Rotate","IInkStrokes::Rotate","Rotate","Rotate method [Tablet PC]","Rotate method [Tablet PC]","IInkStrokes interface","msinkaut/IInkStrokes::Rotate","tablet.inkstrokes_rotate"]
old-location: tablet\inkstrokes_rotate.htm
tech.root: tablet
ms.assetid: d198215d-9504-4c87-addb-63d863a6ede3
ms.date: 12/05/2018
ms.keywords: 3b3d5a58-31e8-4d0e-a1c9-25bb36bb8d9c, IInkStrokes interface [Tablet PC],Rotate method, IInkStrokes.Rotate, IInkStrokes::Rotate, Rotate, Rotate method [Tablet PC], Rotate method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::Rotate, tablet.inkstrokes_rotate
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
 - IInkStrokes::Rotate
 - msinkaut/IInkStrokes::Rotate
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
 - IInkStrokes.Rotate
---

# IInkStrokes::Rotate


## -description

Rotates the ink using an angle in degrees around a center point of the rotation.

## -parameters

### -param Degrees [in]

The degrees by which to rotate clockwise.

### -param x [in, optional]

Optional. The x-coordinate of the point in ink space coordinates around which to rotate. Default is the origin.

### -param y [in, optional]

Optional. The y-coordinate of the point in ink space coordinates around which to rotate. Default is the origin.

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

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
