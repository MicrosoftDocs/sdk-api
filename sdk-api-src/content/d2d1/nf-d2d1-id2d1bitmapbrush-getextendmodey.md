---
UID: NF:d2d1.ID2D1BitmapBrush.GetExtendModeY
title: ID2D1BitmapBrush::GetExtendModeY (d2d1.h)
description: Gets the method by which the brush vertically tiles those areas that extend past its bitmap.
helpviewer_keywords: ["GetExtendModeY","GetExtendModeY method [Direct2D]","GetExtendModeY method [Direct2D]","ID2D1BitmapBrush interface","ID2D1BitmapBrush interface [Direct2D]","GetExtendModeY method","ID2D1BitmapBrush.GetExtendModeY","ID2D1BitmapBrush::GetExtendModeY","d2d1/ID2D1BitmapBrush::GetExtendModeY","direct2d.ID2D1BitmapBrush_GetExtendModeY"]
old-location: direct2d\ID2D1BitmapBrush_GetExtendModeY.htm
tech.root: Direct2D
ms.assetid: e71fef61-9d6a-441b-a88f-9f2cead23ecd
ms.date: 12/05/2018
ms.keywords: GetExtendModeY, GetExtendModeY method [Direct2D], GetExtendModeY method [Direct2D],ID2D1BitmapBrush interface, ID2D1BitmapBrush interface [Direct2D],GetExtendModeY method, ID2D1BitmapBrush.GetExtendModeY, ID2D1BitmapBrush::GetExtendModeY, d2d1/ID2D1BitmapBrush::GetExtendModeY, direct2d.ID2D1BitmapBrush_GetExtendModeY
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1BitmapBrush::GetExtendModeY
 - d2d1/ID2D1BitmapBrush::GetExtendModeY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1BitmapBrush.GetExtendModeY
---

# ID2D1BitmapBrush::GetExtendModeY


## -description

  Gets the method by which the brush vertically tiles those areas that extend past its bitmap.



## -returns

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap.

## -remarks

Like all brushes, <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> defines an infinite plane of content. 

 Because bitmaps are finite, it relies on an extend mode to determine how the plane is filled horizontally and vertically.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey">ID2D1BitmapBrush::SetExtendModeY</a>

