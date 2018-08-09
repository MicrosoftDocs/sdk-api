---
UID: NF:segment.IMSVidRect.get_Width
title: IMSVidRect::get_Width
author: windows-sdk-content
description: The get_Width method retrieves the width of the rectangle.
old-location: mstv\imsvidrect_get_width.htm
old-project: mstv
ms.assetid: 7b1d07b8-41e4-44f8-8c28-377c7a9e463d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Width method, IMSVidRect.get_Width, IMSVidRect::get_Width, IMSVidRectget_Width, get_Width, get_Width method [Microsoft TV Technologies], get_Width method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_width, segment/IMSVidRect::get_Width
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidRect.get_Width
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidRect::get_Width


## -description


The <b>get_Width</b> method retrieves the width of the rectangle.


## -parameters




### -param WidthVal






#### - pWidthVal [out]

Pointer to a variable that receives the width, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Calling the <a href="https://msdn.microsoft.com/8e61fd8a-9ea0-48c1-8749-780b0363c12d">IMSVidRect::put_Left</a> method changes the width of the rectangle. For example, if the x-coordinate is zero and the width is 100, setting the x-coordinate to 10 changes the width to 90.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/35eed36a-de3e-4bb6-8b1b-179ba72b568a">IMSVidRect::put_Width</a>
 

 

