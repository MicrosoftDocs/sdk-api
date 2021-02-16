---
UID: NF:d2d1.ID2D1Bitmap.GetDpi
title: ID2D1Bitmap::GetDpi (d2d1.h)
description: Return the dots per inch (DPI) of the bitmap.
helpviewer_keywords: ["GetDpi","GetDpi method [Direct2D]","GetDpi method [Direct2D]","ID2D1Bitmap interface","ID2D1Bitmap interface [Direct2D]","GetDpi method","ID2D1Bitmap.GetDpi","ID2D1Bitmap::GetDpi","d2d1/ID2D1Bitmap::GetDpi","direct2d.ID2D1Bitmap_GetDpi"]
old-location: direct2d\ID2D1Bitmap_GetDpi.htm
tech.root: Direct2D
ms.assetid: 50659165-86e9-4143-af88-a68e422a74e0
ms.date: 12/05/2018
ms.keywords: GetDpi, GetDpi method [Direct2D], GetDpi method [Direct2D],ID2D1Bitmap interface, ID2D1Bitmap interface [Direct2D],GetDpi method, ID2D1Bitmap.GetDpi, ID2D1Bitmap::GetDpi, d2d1/ID2D1Bitmap::GetDpi, direct2d.ID2D1Bitmap_GetDpi
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
 - ID2D1Bitmap::GetDpi
 - d2d1/ID2D1Bitmap::GetDpi
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
 - ID2D1Bitmap.GetDpi
---

# ID2D1Bitmap::GetDpi


## -description

Return the dots per inch (DPI) of the bitmap.

## -parameters

### -param dpiX [out]

Type: <b>FLOAT*</b>

The horizontal DPI of the image. You must allocate storage for this parameter.

### -param dpiY [out]

Type: <b>FLOAT*</b>

The vertical DPI of the image.  You must allocate storage for this parameter.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>

