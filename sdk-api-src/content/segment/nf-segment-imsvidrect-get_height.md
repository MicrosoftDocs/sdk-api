---
UID: NF:segment.IMSVidRect.get_Height
title: IMSVidRect::get_Height
author: windows-sdk-content
description: The get_Height method retrieves the height of the rectangle.
old-location: mstv\imsvidrect_get_height.htm
tech.root: MSTV
ms.assetid: 83925bca-8cb2-4f79-9aca-1bee0fb4a96a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Height method, IMSVidRect.get_Height, IMSVidRect::get_Height, IMSVidRectget_Height, get_Height, get_Height method [Microsoft TV Technologies], get_Height method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_height, segment/IMSVidRect::get_Height
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidRect.get_Height
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidRect::get_Height


## -description


The <b>get_Height</b> method retrieves the height of the rectangle.


## -parameters




### -param HeightVal

TBD




#### - pHeightVal [out]

Pointer to a variable that receives the height, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Calling the <a href="https://msdn.microsoft.com/ee3dbbd2-a8b4-496b-84e6-b0d7615f6a1e">IMSVidRect::put_Top</a> method changes the height of the rectangle. For example, if the y-coordinate is zero and the height is 100, setting the y-coordinate to 10 changes the height to 90.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/410c5d1c-d4e6-460a-b17d-54bfcee10a66">IMSVidRect::put_Height</a>
 

 

