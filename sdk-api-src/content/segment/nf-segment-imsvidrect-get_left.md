---
UID: NF:segment.IMSVidRect.get_Left
title: IMSVidRect::get_Left (segment.h)
author: windows-sdk-content
description: The get_Left method retrieves the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
old-location: mstv\imsvidrect_get_left.htm
tech.root: mstv
ms.assetid: 9e64e560-033b-475a-a281-57af5f893e65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Left method, IMSVidRect.get_Left, IMSVidRect::get_Left, IMSVidRectget_Left, get_Left, get_Left method [Microsoft TV Technologies], get_Left method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_left, segment/IMSVidRect::get_Left
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
 - IMSVidRect.get_Left
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidRect::get_Left


## -description


The <b>get_Left</b> method retrieves the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.


## -parameters




### -param LeftVal [out]

Pointer to a variable that receives the left x-coordinate, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694605(v=VS.85).aspx">IMSVidRect::get_HWnd</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694611(v=VS.85).aspx">IMSVidRect::put_Left</a>
 

 

