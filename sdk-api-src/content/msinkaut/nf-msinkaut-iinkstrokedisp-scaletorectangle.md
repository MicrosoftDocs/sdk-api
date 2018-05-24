---
UID: NF:msinkaut.IInkStrokeDisp.ScaleToRectangle
title: IInkStrokeDisp::ScaleToRectangle
author: windows-driver-content
description: Scales the IInkStrokeDisp object or InkStrokes collection to fit in the specified InkRectangle object.
old-location: tablet\iinkstrokedisp_scaletorectangle.htm
old-project: tablet
ms.assetid: 8bc22004-3781-4018-9a92-88958039248c
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 8bc22004-3781-4018-9a92-88958039248c, IInkStrokeDisp interface [Tablet PC],ScaleToRectangle method, IInkStrokeDisp.ScaleToRectangle, IInkStrokeDisp::ScaleToRectangle, ScaleToRectangle, ScaleToRectangle method [Tablet PC], ScaleToRectangle method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::ScaleToRectangle, tablet.iinkstrokedisp_scaletorectangle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.ScaleToRectangle
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokeDisp::ScaleToRectangle


## -description



Scales the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to fit in the specified <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a> object.




## -parameters




### -param Rectangle [in]

The <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a> in ink space to which the stroke or collection of strokes is scaled. The strokes are scaled and translated to match the strokes' bounding box to the rectangle.


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
 




## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>
 

 

