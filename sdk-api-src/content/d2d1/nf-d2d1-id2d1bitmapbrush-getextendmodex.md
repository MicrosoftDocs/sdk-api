---
UID: NF:d2d1.ID2D1BitmapBrush.GetExtendModeX
title: ID2D1BitmapBrush::GetExtendModeX (d2d1.h)
author: windows-sdk-content
description: Gets the method by which the brush horizontally tiles those areas that extend past its bitmap.
old-location: direct2d\ID2D1BitmapBrush_GetExtendModeX.htm
tech.root: Direct2D
ms.assetid: 167c5aff-b070-4020-87c4-1385e014f22a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetExtendModeX, GetExtendModeX method [Direct2D], GetExtendModeX method [Direct2D],ID2D1BitmapBrush interface, ID2D1BitmapBrush interface [Direct2D],GetExtendModeX method, ID2D1BitmapBrush.GetExtendModeX, ID2D1BitmapBrush::GetExtendModeX, d2d1/ID2D1BitmapBrush::GetExtendModeX, direct2d.ID2D1BitmapBrush_GetExtendModeX
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
ms.custom: 19H1
---

# ID2D1BitmapBrush::GetExtendModeX


## -description


  Gets the method by which the brush horizontally tiles those areas that extend past its bitmap.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap.




## -remarks



Like all brushes, <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> defines an infinite plane of content. Because bitmaps are finite, it relies on an extend mode to determine how the plane is filled horizontally and vertically.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex">ID2D1BitmapBrush::SetExtendModeX</a>
 

 

