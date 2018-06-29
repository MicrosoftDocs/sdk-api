---
UID: NF:msinkaut.IInkOverlay.Draw
title: IInkOverlay::Draw
author: windows-sdk-content
description: Sets a rectangle in which to redraw the ink within the InkOverlay object.
old-location: tablet\inkoverlay_draw.htm
old-project: tablet
ms.assetid: 80c2de5c-c6ce-4f51-9bd5-5fcf16fd4bcb
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: 80c2de5c-c6ce-4f51-9bd5-5fcf16fd4bcb, Draw, Draw method [Tablet PC], Draw method [Tablet PC],IInkOverlay interface, IInkOverlay, IInkOverlay interface [Tablet PC],Draw method, IInkOverlay.Draw, IInkOverlay::Draw, msinkaut/IInkOverlay::Draw, tablet.inkoverlay_draw
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
 - IInkOverlay.Draw
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::Draw


## -description



Sets a rectangle in which to redraw the ink within the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object.




## -parameters




### -param Rect [in]

The rectangle on which to draw, in pixel coordinates. When this parameter is <b>NULL</b>, the entire window is redrawn.


## -returns



This method can return one of these values.




## -remarks




<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> within the rectangle represented by <i>rDrawRect</i> is drawn when the area is next repainted if the <a href="https://msdn.microsoft.com/f5cb889e-75db-416e-9754-a96f65dad6ed">AutoRedraw</a> property is <b>TRUE</b>.




## -see-also




<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>
 

 

