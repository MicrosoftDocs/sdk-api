---
UID: NF:msinkaut.IInkRenderer.Rotate
title: IInkRenderer::Rotate (msinkaut.h)
description: Applies a rotation to a InkRenderer's view transform.
helpviewer_keywords: ["1928c81a-c618-4afd-b0eb-06e7b8b80431","IInkRenderer interface [Tablet PC]","Rotate method","IInkRenderer.Rotate","IInkRenderer::Rotate","Rotate","Rotate method [Tablet PC]","Rotate method [Tablet PC]","IInkRenderer interface","msinkaut/IInkRenderer::Rotate","tablet.inkrenderer_rotate"]
old-location: tablet\inkrenderer_rotate.htm
tech.root: tablet
ms.assetid: 1928c81a-c618-4afd-b0eb-06e7b8b80431
ms.date: 12/05/2018
ms.keywords: 1928c81a-c618-4afd-b0eb-06e7b8b80431, IInkRenderer interface [Tablet PC],Rotate method, IInkRenderer.Rotate, IInkRenderer::Rotate, Rotate, Rotate method [Tablet PC], Rotate method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::Rotate, tablet.inkrenderer_rotate
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
 - IInkRenderer::Rotate
 - msinkaut/IInkRenderer::Rotate
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
 - IInkRenderer.Rotate
---

# IInkRenderer::Rotate


## -description

Applies a rotation to a <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a>'s view transform.

## -parameters

### -param Degrees [in]

The degrees by which to rotate clockwise.

### -param x [in, optional]

Optional. The x-coordinate of the point in ink space coordinates around which to rotate. The default is zero.

### -param y [in, optional]

Optional. The y-coordinate of the point in ink space coordinates around which to rotate. The default is zero.

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

If no point is specified, the rotation is centered around the origin.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>
