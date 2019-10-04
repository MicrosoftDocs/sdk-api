---
UID: NF:d2d1.ID2D1BitmapBrush.SetExtendModeY
title: ID2D1BitmapBrush::SetExtendModeY (d2d1.h)
author: windows-sdk-content
description: Specifies how the brush vertically tiles those areas that extend past its bitmap.
old-location: direct2d\ID2D1BitmapBrush_SetExtendModeY.htm
tech.root: Direct2D
ms.assetid: 6039ad41-e4b4-41e2-a4b1-31ad93ba88fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetExtendModeY method, ID2D1BitmapBrush.SetExtendModeY, ID2D1BitmapBrush::SetExtendModeY, SetExtendModeY, SetExtendModeY method [Direct2D], SetExtendModeY method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetExtendModeY, direct2d.ID2D1BitmapBrush_SetExtendModeY
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1BitmapBrush.SetExtendModeY"
dev_langs:
 - c++
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
 - ID2D1BitmapBrush.SetExtendModeY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1BitmapBrush::SetExtendModeY


## -description


Specifies how the brush vertically tiles those areas that extend past its bitmap.


## -parameters




### -param extendModeY

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap.


## -returns



This method does not return a value.




## -remarks



Sometimes, the  bitmap for a bitmap brush doesn't completely fill the area being painted. When this happens, Direct2D uses the brush's horizontal (<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex">SetExtendModeX</a>) and vertical (<b>SetExtendModeY</b>) extend mode settings to determine how to fill the remaining area.

The following illustration shows the results from  every  possible combination of the extend modes for an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>: <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE_CLAMP</a> (CLAMP), <b>D2D1_EXTEND_MODE_WRAP</b> (WRAP), and <b>D2D1_EXTEND_MIRROR</b> (MIRROR).

<img alt="Illustration of a bitmap and the resulting images from various extend modes" src="./images/bitmapwrap_clamp_mirror.png"/>


#### Examples

The following example shows how to set the bitmap brush's x- and y-extend modes to <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MIRROR</a>. It  then paints the rectangle with the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>.

It produces the following output.

<img alt="Illustration of an original image and the resulting image from setting both x- and y- extend modes to mirror" src="./images/brushes_ovw_bitmapmirrormirror.png"/>


```cpp
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);

```


For more information about bitmap brushes, see the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmapbrush-getextendmodey">ID2D1BitmapBrush::GetExtendModeY</a>
 

 

