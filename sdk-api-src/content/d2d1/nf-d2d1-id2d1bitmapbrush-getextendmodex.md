---
UID: NF:d2d1.ID2D1BitmapBrush.GetExtendModeX
title: ID2D1BitmapBrush::GetExtendModeX
author: windows-sdk-content
description: Gets the method by which the brush horizontally tiles those areas that extend past its bitmap.
old-location: direct2d\ID2D1BitmapBrush_GetExtendModeX.htm
tech.root: direct2d
ms.assetid: 167c5aff-b070-4020-87c4-1385e014f22a
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetExtendModeX, GetExtendModeX method [Direct2D], GetExtendModeX method [Direct2D],ID2D1BitmapBrush interface, ID2D1BitmapBrush interface [Direct2D],GetExtendModeX method, ID2D1BitmapBrush.GetExtendModeX, ID2D1BitmapBrush::GetExtendModeX, d2d1/ID2D1BitmapBrush::GetExtendModeX, direct2d.ID2D1BitmapBrush_GetExtendModeX
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1BitmapBrush.GetExtendModeX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BitmapBrush::GetExtendModeX


## -description


  Gets the method by which the brush horizontally tiles those areas that extend past its bitmap.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap.




## -remarks



Like all brushes, <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> defines an infinite plane of content. Because bitmaps are finite, it relies on an extend mode to determine how the plane is filled horizontally and vertically.




## -see-also




<a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>



<a href="https://msdn.microsoft.com/bb20c9ea-a2b1-4fa5-a0e3-b788fe493993">ID2D1BitmapBrush::SetExtendModeX</a>
 

 

