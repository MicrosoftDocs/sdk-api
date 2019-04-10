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
---

# ID2D1Bitmap::GetSize


## -description


Returns the size, in device-independent pixels (DIPs), of the bitmap.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The size, in DIPs, of the bitmap.




## -remarks



A DIP is 1/96 of an inch. To retrieve the size in device pixels, use the <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap::GetPixelSize</a>method.




## -see-also




<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>



<a href="https://msdn.microsoft.com/0d51408a-2648-4984-bbc0-9846d5161c77">ID2D1Bitmap::GetPixelSize</a>
 

 

