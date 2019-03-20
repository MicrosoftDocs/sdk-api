---
UID: NF:d2d1.ID2D1BitmapBrush.GetExtendModeY
title: ID2D1BitmapBrush::GetExtendModeY (d2d1.h)
author: windows-sdk-content
description: Gets the method by which the brush vertically tiles those areas that extend past its bitmap.
old-location: direct2d\ID2D1BitmapBrush_GetExtendModeY.htm
tech.root: Direct2D
ms.assetid: e71fef61-9d6a-441b-a88f-9f2cead23ecd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetExtendModeY, GetExtendModeY method [Direct2D], GetExtendModeY method [Direct2D],ID2D1BitmapBrush interface, ID2D1BitmapBrush interface [Direct2D],GetExtendModeY method, ID2D1BitmapBrush.GetExtendModeY, ID2D1BitmapBrush::GetExtendModeY, d2d1/ID2D1BitmapBrush::GetExtendModeY, direct2d.ID2D1BitmapBrush_GetExtendModeY
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
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
 - ID2D1BitmapBrush.GetExtendModeY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BitmapBrush::GetExtendModeY


## -description


  Gets the method by which the brush vertically tiles those areas that extend past its bitmap.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap.




## -remarks



Like all brushes, <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> defines an infinite plane of content. 

 Because bitmaps are finite, it relies on an extend mode to determine how the plane is filled horizontally and vertically.




## -see-also




<a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>



<a href="https://msdn.microsoft.com/6039ad41-e4b4-41e2-a4b1-31ad93ba88fd">ID2D1BitmapBrush::SetExtendModeY</a>
 

 

