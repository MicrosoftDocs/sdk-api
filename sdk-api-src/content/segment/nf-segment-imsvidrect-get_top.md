---
UID: NF:segment.IMSVidRect.get_Top
title: IMSVidRect::get_Top
author: windows-sdk-content
description: The get_Top method retrieves the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.
old-location: mstv\imsvidrect_get_top.htm
old-project: mstv
ms.assetid: 3596141c-e359-4ea5-8d6a-9ec374c1f854
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidRect interface [Microsoft TV Technologies],get_Top method, IMSVidRect.get_Top, IMSVidRect::get_Top, IMSVidRectget_Top, get_Top, get_Top method [Microsoft TV Technologies], get_Top method [Microsoft TV Technologies],IMSVidRect interface, mstv.imsvidrect_get_top, segment/IMSVidRect::get_Top
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
 - IMSVidRect.get_Top
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidRect::get_Top


## -description


The <b>get_Top</b> method retrieves the top y-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.


## -parameters




### -param TopVal






#### - pTopVal [out]

Pointer to a variable that receives the top y-coordinate, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/caa56beb-7eba-48a1-8645-f63666ba0593">IMSVidRect::get_HWnd</a>



<a href="https://msdn.microsoft.com/ee3dbbd2-a8b4-496b-84e6-b0d7615f6a1e">IMSVidRect::put_Top</a>
 

 

