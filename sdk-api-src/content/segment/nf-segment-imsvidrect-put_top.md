---
UID: NF:segment.IMSVidRect.put_Top
title: IMSVidRect::put_Top
author: windows-driver-content
description: The put_Top method specifies the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
old-location: mstv\imsvidrect_put_top.htm
old-project: mstv
ms.assetid: ee3dbbd2-a8b4-496b-84e6-b0d7615f6a1e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],put_Top method, IMSVidRect.put_Top, IMSVidRect::put_Top, IMSVidRectput_Top, mstv.imsvidrect_put_top, put_Top, put_Top method [Microsoft TV Technologies], put_Top method [Microsoft TV Technologies],IMSVidRect interface, segment/IMSVidRect::put_Top
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidRect.put_Top
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidRect::put_Top


## -description


The <b>put_Top</b> method specifies the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.


## -parameters




### -param TopVal [in]

Specifies the top y-coordinate, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Setting the top y-coordinate also changes the height of the rectangle. For example, if the y-coordinate is zero and the height is 100, setting the y-coordinate to 10 changes the height to 90.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/caa56beb-7eba-48a1-8645-f63666ba0593">IMSVidRect::get_HWnd</a>



<a href="https://msdn.microsoft.com/3596141c-e359-4ea5-8d6a-9ec374c1f854">IMSVidRect::get_Top</a>
 

 

