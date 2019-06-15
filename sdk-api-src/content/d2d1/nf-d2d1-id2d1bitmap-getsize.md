---
UID: NF:d2d1.ID2D1Bitmap.GetSize
title: ID2D1Bitmap::GetSize (d2d1.h)
author: windows-sdk-content
description: Returns the size, in device-independent pixels (DIPs), of the bitmap.
old-location: direct2d\ID2D1Bitmap_GetSize.htm
tech.root: Direct2D
ms.assetid: 6ab1d67d-d7ee-41a0-a298-738b1520ff3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [Direct2D], GetSize method [Direct2D],ID2D1Bitmap interface, ID2D1Bitmap interface [Direct2D],GetSize method, ID2D1Bitmap.GetSize, ID2D1Bitmap::GetSize, d2d1/ID2D1Bitmap::GetSize, direct2d.ID2D1Bitmap_GetSize
ms.topic: method
f1_keywords: ["d2d1/ID2D1Bitmap.GetSize"]
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
 - ID2D1Bitmap.GetSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Bitmap::GetSize


## -description


Returns the size, in device-independent pixels (DIPs), of the bitmap.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-size-f">D2D1_SIZE_F</a></b>

The size, in DIPs, of the bitmap.




## -remarks



A DIP is 1/96 of an inch. To retrieve the size in device pixels, use the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap::GetPixelSize</a>method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmap-getpixelsize">ID2D1Bitmap::GetPixelSize</a>
 

 

