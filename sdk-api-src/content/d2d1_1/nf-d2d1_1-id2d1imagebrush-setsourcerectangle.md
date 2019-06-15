---
UID: NF:d2d1_1.ID2D1ImageBrush.SetSourceRectangle
title: ID2D1ImageBrush::SetSourceRectangle (d2d1_1.h)
author: windows-sdk-content
description: Sets the source rectangle in the image brush.
old-location: direct2d\id2d1imagebrush_setsourcerectangle.htm
tech.root: Direct2D
ms.assetid: be445505-585f-448b-a7eb-386e18a416b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1ImageBrush interface [Direct2D],SetSourceRectangle method, ID2D1ImageBrush.SetSourceRectangle, ID2D1ImageBrush::SetSourceRectangle, SetSourceRectangle, SetSourceRectangle method [Direct2D], SetSourceRectangle method [Direct2D],ID2D1ImageBrush interface, d2d1_1/ID2D1ImageBrush::SetSourceRectangle, direct2d.id2d1imagebrush_setsourcerectangle
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1ImageBrush.SetSourceRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1ImageBrush::SetSourceRectangle


## -description


Sets the source rectangle in the image brush.


## -parameters




### -param sourceRectangle [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The source rectangle that defines the portion of the image to tile.


## -returns



This method does not return a value.




## -remarks



The top left corner of the <i>sourceRectangle</i> parameter maps to the brush space origin. That is, if the  brush and world transforms are both identity, the portion of the image in the top left corner of the source rectangle will be rendered at (0,0) in the render target.

The source rectangle will be expanded differently depending on whether the input image is based on   pixels (a bitmap or effect) or by a command list.



<ul>
<li>If the input image is a bitmap or an effect, the rectangle will be expanded to encapsulate a full input pixel before being additionally down-scaled to ensure that the projected rectangle will be correct in the final scene-space.</li>
<li>If the input image is a command list, the command list will be slightly expanded to encapsulate a full input pixel.
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1imagebrush">ID2D1ImageBrush</a>
 

 

