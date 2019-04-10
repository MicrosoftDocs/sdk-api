---
UID: NF:segment.IMSVidRect.put_Left
title: IMSVidRect::put_Left (segment.h)
author: windows-sdk-content
description: The put_Left method specifies the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
old-location: mstv\imsvidrect_put_left.htm
tech.root: mstv
ms.assetid: 8e61fd8a-9ea0-48c1-8749-780b0363c12d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],put_Left method, IMSVidRect.put_Left, IMSVidRect::put_Left, IMSVidRectput_Left, mstv.imsvidrect_put_left, put_Left, put_Left method [Microsoft TV Technologies], put_Left method [Microsoft TV Technologies],IMSVidRect interface, segment/IMSVidRect::put_Left
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
 - IMSVidRect.put_Left
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidRect::put_Left


## -description


The <b>put_Left</b> method specifies the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.


## -parameters




### -param LeftVal [in]

Specifies the left x-coordinate, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Setting the left x-coordinate also changes the width of the rectangle. For example, if the x-coordinate is zero and the width is 100, setting the x-coordinate to 10 changes the width to 90.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694605(v=VS.85).aspx">IMSVidRect::get_HWnd</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694606(v=VS.85).aspx">IMSVidRect::get_Left</a>
 

 

