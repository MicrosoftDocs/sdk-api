---
UID: NF:msinkaut.IInkStrokes.Transform
title: IInkStrokes::Transform
author: windows-sdk-content
description: Applies a linear transformation to an IInkStrokeDisp object or an InkStrokes collection, which can represent scaling, rotation, translation, and combinations of transformations.
old-location: tablet\inkstrokes_transform.htm
old-project: tablet
ms.assetid: 910ae16d-be9a-422c-b9af-9a2df28df463
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInkStrokes interface [Tablet PC],Transform method, IInkStrokes.Transform, IInkStrokes::Transform, Transform, Transform method [Tablet PC], Transform method [Tablet PC],IInkStrokes interface, b7860215-a267-407e-9105-8e51340f4216, msinkaut/IInkStrokes::Transform, tablet.inkstrokes_transform
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
 - IInkStrokes.Transform
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokes::Transform


## -description



Applies a linear transformation to an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection, which can represent scaling, rotation, translation, and combinations of transformations.




## -parameters




### -param Transform [in]

The transform to use on the stroke or strokes. (This is an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object, which correlates to the <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure). The transformation applies to both the points and pen width (if <i>ApplyOnPenWidth</i> is <b>VARIANT_TRUE</b>).


### -param ApplyOnPenWidth [in, optional]

Optional. <b>VARIANT_TRUE</b> to apply the transform to the width of the ink in the <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> of the strokes; otherwise, <b>VARIANT_FALSE</b>. The default is <b>VARIANT_FALSE</b>.


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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

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




<a href="https://msdn.microsoft.com/en-us/library/Mt846806(v=VS.85).aspx">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

