---
UID: NF:gdipluslinecaps.AdjustableArrowCap.AdjustableArrowCap(const AdjustableArrowCap &)
title: AdjustableArrowCap::AdjustableArrowCap(const AdjustableArrowCap &)
author: windows-sdk-content
description: Creates an adjustable arrow line cap with the specified height and width. The arrow line cap can be filled or nonfilled. The middle inset defaults to zero.
old-location: gdiplus\_gdiplus_CLASS_AdjustableArrowCap_AdjustableArrowCap_height_width_isFilled_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\adjustablearrowcapclass\adjustablearrowcap_91height_width_isfilled.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: AdjustableArrowCap, AdjustableArrowCap class [GDI+],AdjustableArrowCap constructor, AdjustableArrowCap constructor [GDI+], AdjustableArrowCap constructor [GDI+],AdjustableArrowCap class, AdjustableArrowCap.AdjustableArrowCap, AdjustableArrowCap.AdjustableArrowCap(const AdjustableArrowCap &), AdjustableArrowCap::AdjustableArrowCap, AdjustableArrowCap::AdjustableArrowCap(const AdjustableArrowCap &), _gdiplus_CLASS_AdjustableArrowCap_AdjustableArrowCap_height_width_isFilled_, gdiplus._gdiplus_CLASS_AdjustableArrowCap_AdjustableArrowCap_height_width_isFilled_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluslinecaps.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - AdjustableArrowCap.AdjustableArrowCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# AdjustableArrowCap::AdjustableArrowCap(const AdjustableArrowCap &)


## -description


Creates an adjustable arrow line cap with the specified height and width. The arrow line cap can be filled or nonfilled. The middle inset defaults to zero.


## -parameters






#### - height [in]

Type: <b>REAL</b>

Real number that specifies the length, in units, of the arrow from its base to its point. 


#### - isFilled [in]

Type: <b>BOOL</b>

Boolean value that specifies whether the arrow is filled. The default value is <b>TRUE</b>. 


#### - width [in]

Type: <b>REAL</b>

Real number that specifies the distance, in units, between the corners of the base of the arrow. 


## -remarks



The middle inset is the number of units that the midpoint of the base shifts towards the vertex. A middle inset of zero results in no shift — the base is a straight line, giving the arrow a triangular shape. A positive (greater than zero) middle inset results in a shift the specified number of units toward the vertex — the base is an arrow shape that points toward the vertex, giving the arrow cap a V-shape. A negative (less than zero) middle inset results in a shift the specified number of units away from the vertex — the base becomes an arrow shape that points away from the vertex, giving the arrow either a diamond shape (if the absolute value of the middle inset is equal to the height) or distorted diamond shape. If the middle inset is equal to or greater than the height of the arrow cap, the cap does not appear at all. The value of the middle inset affects the arrow cap only if the arrow cap is filled. The middle inset defaults to zero when an <b>AdjustableArrowCap::AdjustableArrowCap</b> object is constructed.




## -see-also




<a href="https://msdn.microsoft.com/da4a0644-eedf-4a9c-935a-e9fa822b2673">AdjustableArrowCap</a>



<a href="https://msdn.microsoft.com/83bc6530-9d78-49ad-9dfc-ea9776945ae6">AdjustableArrowCap::GetMiddleInset</a>



<a href="https://msdn.microsoft.com/67721251-b805-425f-9742-6afed25df831">AdjustableArrowCap::SetMiddleInset</a>
 

 

