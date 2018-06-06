---
UID: NF:msinkaut.IInkRenderer.GetViewTransform
title: IInkRenderer::GetViewTransform
author: windows-sdk-content
description: Gets the InkTransform object that represents the view transform that is used to render ink.
old-location: tablet\inkrenderer_getviewtransform.htm
old-project: tablet
ms.assetid: 8a4d768d-09b6-45e1-b412-e267d92cc3ef
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 8a4d768d-09b6-45e1-b412-e267d92cc3ef, GetViewTransform, GetViewTransform method [Tablet PC], GetViewTransform method [Tablet PC],IInkRenderer interface, IInkRenderer interface [Tablet PC],GetViewTransform method, IInkRenderer.GetViewTransform, IInkRenderer::GetViewTransform, msinkaut/IInkRenderer::GetViewTransform, tablet.inkrenderer_getviewtransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRenderer.GetViewTransform
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRenderer::GetViewTransform


## -description



Gets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the view transform that is used to render ink.




## -parameters




### -param ViewTransform [in]

 The matrix that represents the geometric transformation - rotation, scaling, shear, and reflection - values to use to transform the stroke coordinates within the ink space. The transformation applies to both the points and pen width. View transformation occurs after object transformation.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



Any translations applied to this transform should be in ink space units (1 unit = .01mm).

Adjusting the view transform is analogous to adjusting the zoom factor on the ink rendering.

View transformation occurs after object transformation.




## -see-also




<a href="https://msdn.microsoft.com/11195fa1-ca59-4da6-8454-6209c75ccc67">GetObjectTransform Method</a>



<a href="tablet.iinkrenderer">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>



<a href="https://msdn.microsoft.com/8d0cbc97-d9a2-4b6c-8e92-55237cef6523">SetObjectTransform Method</a>



<a href="https://msdn.microsoft.com/b1850d41-4523-4a2b-a7ae-6b85d1ae9a97">SetViewTransform Method</a>
 

 

