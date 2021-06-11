---
UID: NF:msinkaut.IInkRenderer.SetViewTransform
title: IInkRenderer::SetViewTransform (msinkaut.h)
description: Sets the InkTransform object that represents the view transform that is used to render ink.
helpviewer_keywords: ["IInkRenderer interface [Tablet PC]","SetViewTransform method","IInkRenderer.SetViewTransform","IInkRenderer::SetViewTransform","SetViewTransform","SetViewTransform method [Tablet PC]","SetViewTransform method [Tablet PC]","IInkRenderer interface","b1850d41-4523-4a2b-a7ae-6b85d1ae9a97","msinkaut/IInkRenderer::SetViewTransform","tablet.inkrenderer_setviewtransform"]
old-location: tablet\inkrenderer_setviewtransform.htm
tech.root: tablet
ms.assetid: b1850d41-4523-4a2b-a7ae-6b85d1ae9a97
ms.date: 12/05/2018
ms.keywords: IInkRenderer interface [Tablet PC],SetViewTransform method, IInkRenderer.SetViewTransform, IInkRenderer::SetViewTransform, SetViewTransform, SetViewTransform method [Tablet PC], SetViewTransform method [Tablet PC],IInkRenderer interface, b1850d41-4523-4a2b-a7ae-6b85d1ae9a97, msinkaut/IInkRenderer::SetViewTransform, tablet.inkrenderer_setviewtransform
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
 - IInkRenderer::SetViewTransform
 - msinkaut/IInkRenderer::SetViewTransform
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
 - IInkRenderer.SetViewTransform
---

# IInkRenderer::SetViewTransform


## -description

Sets the <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the view transform that is used to render ink.

## -parameters

### -param ViewTransform [in]

The <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the geometric transformation - rotation, scaling, shear, and reflection - values to use to transform the stroke coordinates within the ink space.

A <b>NULL</b> value for the <i>viewTransform</i> parameter correlates to the identity transform.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>viewTransform</i> does not point to a compatible <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

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

The transformation applies to both the points and pen width.

View transformation occurs after object transformation.

The pen width is calculated by multiplying the specified pen width (or default of 53, if unspecified) by the square root of the determinant of the view transform.

It is problematic to call this method in response to SENT message.  Test whether you are processing a SENT message
			  by calling <a href="/windows/desktop/api/winuser/nf-winuser-insendmessageex">InSendMesssageEx</a> and then POST the message to yourself if the message was SENT.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform">GetObjectTransform Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">GetViewTransform Method</a>



<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>
