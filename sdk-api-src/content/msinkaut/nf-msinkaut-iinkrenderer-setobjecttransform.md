---
UID: NF:msinkaut.IInkRenderer.SetObjectTransform
title: IInkRenderer::SetObjectTransform (msinkaut.h)
description: Sets the InkTransform object that represents the object transform that is used to render ink.
helpviewer_keywords: ["8d0cbc97-d9a2-4b6c-8e92-55237cef6523","IInkRenderer interface [Tablet PC]","SetObjectTransform method","IInkRenderer.SetObjectTransform","IInkRenderer::SetObjectTransform","SetObjectTransform","SetObjectTransform method [Tablet PC]","SetObjectTransform method [Tablet PC]","IInkRenderer interface","msinkaut/IInkRenderer::SetObjectTransform","tablet.inkrenderer_setobjecttransform"]
old-location: tablet\inkrenderer_setobjecttransform.htm
tech.root: tablet
ms.assetid: 8d0cbc97-d9a2-4b6c-8e92-55237cef6523
ms.date: 12/05/2018
ms.keywords: 8d0cbc97-d9a2-4b6c-8e92-55237cef6523, IInkRenderer interface [Tablet PC],SetObjectTransform method, IInkRenderer.SetObjectTransform, IInkRenderer::SetObjectTransform, SetObjectTransform, SetObjectTransform method [Tablet PC], SetObjectTransform method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::SetObjectTransform, tablet.inkrenderer_setobjecttransform
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
 - IInkRenderer::SetObjectTransform
 - msinkaut/IInkRenderer::SetObjectTransform
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
 - IInkRenderer.SetObjectTransform
---

# IInkRenderer::SetObjectTransform


## -description

Sets the <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the object transform that is used to render ink.

## -parameters

### -param ObjectTransform [in]

The <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the geometric transformation - rotation, scaling, shear, and reflection - values to use to transform the stroke coordinates within the ink space.

A <b>NULL</b> value for the <i>objectTransform</i> parameter correlates to the identity transform.

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
<i>objectTransform</i> does not point to a compatible <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

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

The transformation applies to the points, but not the pen width.

Object transformation occurs before view transformation.

It is problematic to call this method in response to SENT message.  Test whether you are processing a SENT message
			  by calling <a href="/windows/desktop/api/winuser/nf-winuser-insendmessageex">InSendMesssageEx</a> and then POST the message to yourself if the message was SENT.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform">GetObjectTransform Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">GetViewTransform Method</a>



<a href="../msinkaut/nn-msinkaut-iinkrenderer.md">IInkRenderer</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform">SetViewTransform Method</a>
