---
UID: NF:msinkaut.IInkRenderer.ScaleTransform
title: IInkRenderer::ScaleTransform
author: windows-sdk-content
description: Scales the view transform in the X and Y dimension.
old-location: tablet\inkrenderer_scaletransform.htm
tech.root: tablet
ms.assetid: 63a7d5f7-2c93-4f45-ad8d-aa3f75f78eff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 63a7d5f7-2c93-4f45-ad8d-aa3f75f78eff, IInkRenderer interface [Tablet PC],ScaleTransform method, IInkRenderer.ScaleTransform, IInkRenderer::ScaleTransform, ScaleTransform, ScaleTransform method [Tablet PC], ScaleTransform method [Tablet PC],IInkRenderer interface, msinkaut/IInkRenderer::ScaleTransform, tablet.inkrenderer_scaletransform
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
 - IInkRenderer.ScaleTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRenderer::ScaleTransform


## -description



Scales the <a href="https://msdn.microsoft.com/8a4d768d-09b6-45e1-b412-e267d92cc3ef">view transform</a> in the X and Y dimension.




## -parameters




### -param HorizontalMultiplier [in]

The factor to scale the X dimension in the view transform.


### -param VerticalMultiplier [in]

The factor to scale the Y dimension in the view transform.


### -param ApplyOnPenWidth [in, optional]

Optional. <b>VARIANT_TRUE</b> to apply the scale factors to the pen width; otherwise, <b>VARIANT_FALSE</b>. The default is <b>VARIANT_TRUE</b>.


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




<a href="https://msdn.microsoft.com/en-us/library/Mt846805(v=VS.85).aspx">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>
 

 

