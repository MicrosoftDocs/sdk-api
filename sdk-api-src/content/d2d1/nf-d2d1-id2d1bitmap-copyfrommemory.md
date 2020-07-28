---
UID: NF:d2d1.ID2D1Bitmap.CopyFromMemory
title: ID2D1Bitmap::CopyFromMemory (d2d1.h)
description: Copies the specified region from memory into the current bitmap.
helpviewer_keywords: ["CopyFromMemory","CopyFromMemory method [Direct2D]","CopyFromMemory method [Direct2D]","ID2D1Bitmap interface","ID2D1Bitmap interface [Direct2D]","CopyFromMemory method","ID2D1Bitmap.CopyFromMemory","ID2D1Bitmap::CopyFromMemory","d2d1/ID2D1Bitmap::CopyFromMemory","direct2d.ID2D1Bitmap_CopyFromMemory"]
old-location: direct2d\ID2D1Bitmap_CopyFromMemory.htm
tech.root: Direct2D
ms.assetid: 594cba56-6f18-439a-ada4-0f591af094bb
ms.date: 12/05/2018
ms.keywords: CopyFromMemory, CopyFromMemory method [Direct2D], CopyFromMemory method [Direct2D],ID2D1Bitmap interface, ID2D1Bitmap interface [Direct2D],CopyFromMemory method, ID2D1Bitmap.CopyFromMemory, ID2D1Bitmap::CopyFromMemory, d2d1/ID2D1Bitmap::CopyFromMemory, direct2d.ID2D1Bitmap_CopyFromMemory
f1_keywords:
- d2d1/ID2D1Bitmap.CopyFromMemory
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
- ID2D1Bitmap.CopyFromMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Bitmap::CopyFromMemory


## -description


Copies the specified region from memory into the current bitmap.


## -parameters




### -param dstRect [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-u">D2D1_RECT_U</a>*</b>

In the current bitmap, the rectangle to which the region specified by <i>srcRect</i> is copied.


### -param srcData [in]

Type: <b>const void*</b>

The data to copy.


### -param pitch

Type: <b>UINT32</b>

The stride, or pitch, of the source bitmap stored in <i>srcData</i>. The stride is the byte count of a scanline (one row of pixels in memory). The stride can be computed from the following formula: pixel width * bytes per pixel + memory padding.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.




## -remarks



This method does not update the size of the current bitmap. If the contents of the source bitmap do not fit in the current bitmap, this method fails. Also, note that this method does not perform format conversion; the two bitmap formats should match. 

If this method is passed invalid input (such as an invalid destination rectangle), can produce unpredictable results, such as a distorted image or device failure.

Calling this method may cause the current batch to flush if the bitmap is active in the batch. If the batch that was flushed does not complete successfully, this method fails. However, this method does not clear the error state of the render target on which the batch was flushed. The failing <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> and tag state will be returned at the next call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a>. 

Starting with Windows 8.1,  this method supports block compressed bitmaps.  If you are using a block compressed format, the end coordinates of the <i>srcRect</i> parameter must be multiples of 4 or the method returns <b>E_INVALIDARG</b>.




## -see-also




<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>
 

 

