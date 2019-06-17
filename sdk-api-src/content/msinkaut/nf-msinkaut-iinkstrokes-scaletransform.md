---
UID: NF:msinkaut.IInkStrokes.ScaleTransform
title: IInkStrokes::ScaleTransform (msinkaut.h)
author: windows-sdk-content
description: Applies the specified horizontal and vertical factors to the transform or ink.
old-location: tablet\inkstrokes_scaletransform.htm
tech.root: tablet
ms.assetid: d7b69554-69e3-4a45-9313-16a3529863e9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkStrokes interface [Tablet PC],ScaleTransform method, IInkStrokes.ScaleTransform, IInkStrokes::ScaleTransform, ScaleTransform, ScaleTransform method [Tablet PC], ScaleTransform method [Tablet PC],IInkStrokes interface, a4140abe-adc8-492d-bb8c-96fba5ca3bd0, msinkaut/IInkStrokes::ScaleTransform, tablet.inkstrokes_scaletransform
ms.topic: method
f1_keywords: ["msinkaut/IInkStrokes.ScaleTransform"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokes.ScaleTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkStrokes::ScaleTransform


## -description



Applies the specified horizontal and vertical factors to the transform or ink.




## -parameters




### -param HorizontalMultiplier [in]

The factor to scale the horizontal dimension in the transform.


### -param VerticalMultiplier [in]

The factor to scale the vertical dimension in the transform.


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



For the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> classes, this method scales the points in the stroke or strokes relative to the origin. Thus, if the <i>HorizontalMultiplier</i> parameter is 2.0, the stroke or strokes will be twice as wide, and will also be twice as far, horizontally, from the origin. To control the relative position of the strokes, use this method in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-move">Move</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846806(v=VS.85).aspx">IInkStrokes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-move">Move Method</a>
 

 

