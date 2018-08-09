---
UID: NE:d2d1.D2D1_EXTEND_MODE
title: D2D1_EXTEND_MODE
author: windows-sdk-content
description: Specifies how a brush paints areas outside of its normal content area.
old-location: direct2d\D2D1_EXTEND_MODE.htm
old-project: direct2d
ms.assetid: 6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_EXTEND_MODE, D2D1_EXTEND_MODE enumeration [Direct2D], D2D1_EXTEND_MODE_CLAMP, D2D1_EXTEND_MODE_MIRROR, D2D1_EXTEND_MODE_WRAP, d2d1/D2D1_EXTEND_MODE, d2d1/D2D1_EXTEND_MODE_CLAMP, d2d1/D2D1_EXTEND_MODE_MIRROR, d2d1/D2D1_EXTEND_MODE_WRAP, direct2d.D2D1_EXTEND_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_EXTEND_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_EXTEND_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_EXTEND_MODE enumeration


## -description


Specifies how a brush paints areas outside of its normal content area.


## -enum-fields




### -field D2D1_EXTEND_MODE_CLAMP

Repeat the edge pixels of the brush's content for all regions outside the normal content area.


### -field D2D1_EXTEND_MODE_WRAP

Repeat the brush's content.


### -field D2D1_EXTEND_MODE_MIRROR

 The same as D2D1_EXTEND_MODE_WRAP, except that alternate tiles of the brush's content are flipped. (The brush's normal content is drawn untransformed.)


### -field D2D1_EXTEND_MODE_FORCE_DWORD




## -remarks



For an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>, the brush's content is the brush's bitmap. For an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>, the brush's content area is the gradient axis. For an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>, the brush's content is the area within the gradient ellipse.  




## -see-also




<a href="https://msdn.microsoft.com/bb20c9ea-a2b1-4fa5-a0e3-b788fe493993">ID2D1BitmapBrush::SetExtendModeX</a>



<a href="https://msdn.microsoft.com/6039ad41-e4b4-41e2-a4b1-31ad93ba88fd">ID2D1BitmapBrush::SetExtendModeY</a>



<a href="https://msdn.microsoft.com/c5f3facf-f1fe-4a47-b283-c0c859d8bc03">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

