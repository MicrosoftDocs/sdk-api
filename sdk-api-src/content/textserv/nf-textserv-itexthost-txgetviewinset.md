---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITextHost::TxGetViewInset


## -description


Requests the dimensions of the white space inset around the text in the text host window.


## -parameters




### -param prc

Type: <b>LPRECT</b>

The inset size, in client coordinates. The top, bottom, left, and right members of the 
					<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure indicate how far in each direction the drawing should be inset. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>.




## -remarks



The view inset is the amount of space on each side between the client rectangle and the view rectangle. The view rectangle (also called the Formatting rectangle) is the rectangle in which the text should be formatted .

The view insets are passed in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure, but this is not really a rectangle. It should be treated as four independent values to subtract on each side of the client rectangle to figure the view rectangle.

The view insets are passed in HIMETRIC (each HIMETRIC unit corresponds to 0.01 millimeter) so that they do not depend on the client rectangle and the rendering device context.

View insets can be negative on either side of the client rectangle, leading to a bigger view rectangle than the client rectangle. The text should then be clipped to the client rectangle. If the view rectangle is wider than the client rectangle, then the host may add a horizontal scroll bar to the control.

Single line–text services objects ignore the right boundary of the view rectangle when formatting text.

The view inset is available from the host at all times, active or inactive.




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

