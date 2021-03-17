---
UID: NF:d2d1.ID2D1BitmapBrush.SetExtendModeX
title: ID2D1BitmapBrush::SetExtendModeX (d2d1.h)
description: Specifies how the brush horizontally tiles those areas that extend past its bitmap.
helpviewer_keywords: ["ID2D1BitmapBrush interface [Direct2D]","SetExtendModeX method","ID2D1BitmapBrush.SetExtendModeX","ID2D1BitmapBrush::SetExtendModeX","SetExtendModeX","SetExtendModeX method [Direct2D]","SetExtendModeX method [Direct2D]","ID2D1BitmapBrush interface","d2d1/ID2D1BitmapBrush::SetExtendModeX","direct2d.ID2D1BitmapBrush_SetExtendModeX"]
old-location: direct2d\ID2D1BitmapBrush_SetExtendModeX.htm
tech.root: Direct2D
ms.assetid: bb20c9ea-a2b1-4fa5-a0e3-b788fe493993
ms.date: 12/05/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetExtendModeX method, ID2D1BitmapBrush.SetExtendModeX, ID2D1BitmapBrush::SetExtendModeX, SetExtendModeX, SetExtendModeX method [Direct2D], SetExtendModeX method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetExtendModeX, direct2d.ID2D1BitmapBrush_SetExtendModeX
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
 - ID2D1BitmapBrush::SetExtendModeX
 - d2d1/ID2D1BitmapBrush::SetExtendModeX
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
 - ID2D1BitmapBrush.SetExtendModeX
---

# ID2D1BitmapBrush::SetExtendModeX


## -description

Specifies how the brush horizontally tiles those areas that extend past its bitmap.

## -parameters

### -param extendModeX

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap.

## -remarks

Sometimes, the  bitmap for a bitmap brush doesn't completely fill the area being painted. When this happens, Direct2D uses the brush's horizontal (<b>SetExtendModeX</b>) and vertical (<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey">SetExtendModeY</a>) extend mode settings to determine how to fill the remaining area.

The following illustration shows the results from  every  possible combination of the extend modes for an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>: <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE_CLAMP</a> (CLAMP), <b>D2D1_EXTEND_MODE_WRAP</b> (WRAP), and <b>D2D1_EXTEND_MIRROR</b> (MIRROR).

<img alt="Illustration of a bitmap and the resulting images from various extend modes" src="./images/bitmapwrap_clamp_mirror.png"/>


## Examples

The following example shows how to set the bitmap brush's x- and y-extend modes to <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MIRROR</a>. It  then paints the rectangle with the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>.

It produces the following output.

<img alt="Illustration an original image and the resulting image from setting both x- and y- extend modes to mirror" src="./images/brushes_ovw_bitmapmirrormirror.png"/>


```cpp
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);

```

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-getextendmodex">ID2D1BitmapBrush::GetExtendModeX</a>

