---
UID: NF:d2d1.ID2D1Bitmap.CopyFromRenderTarget
title: ID2D1Bitmap::CopyFromRenderTarget (d2d1.h)
description: Copies the specified region from the specified render target into the current bitmap.
helpviewer_keywords: ["CopyFromRenderTarget","CopyFromRenderTarget method [Direct2D]","CopyFromRenderTarget method [Direct2D]","ID2D1Bitmap interface","ID2D1Bitmap interface [Direct2D]","CopyFromRenderTarget method","ID2D1Bitmap.CopyFromRenderTarget","ID2D1Bitmap::CopyFromRenderTarget","d2d1/ID2D1Bitmap::CopyFromRenderTarget","direct2d.ID2D1Bitmap_CopyFromRenderTarget"]
old-location: direct2d\ID2D1Bitmap_CopyFromRenderTarget.htm
tech.root: Direct2D
ms.assetid: 42e25099-016e-4656-a412-72dd0fbac1fd
ms.date: 12/05/2018
ms.keywords: CopyFromRenderTarget, CopyFromRenderTarget method [Direct2D], CopyFromRenderTarget method [Direct2D],ID2D1Bitmap interface, ID2D1Bitmap interface [Direct2D],CopyFromRenderTarget method, ID2D1Bitmap.CopyFromRenderTarget, ID2D1Bitmap::CopyFromRenderTarget, d2d1/ID2D1Bitmap::CopyFromRenderTarget, direct2d.ID2D1Bitmap_CopyFromRenderTarget
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
 - ID2D1Bitmap::CopyFromRenderTarget
 - d2d1/ID2D1Bitmap::CopyFromRenderTarget
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
 - ID2D1Bitmap.CopyFromRenderTarget
---

# ID2D1Bitmap::CopyFromRenderTarget


## -description

Copies the specified region from the specified render target into the current bitmap.

## -parameters

### -param destPoint [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-point-2u">D2D1_POINT_2U</a>*</b>

In the current bitmap, the upper-left corner of the area to which the region specified by <i>srcRect</i> is copied.

### -param renderTarget [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>*</b>

The render target that contains the region to copy.

### -param srcRect [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-u">D2D1_RECT_U</a>*</b>

The area of <i>renderTarget</i> to copy.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

This method does not update the size of the current bitmap. If the contents of the source bitmap do not fit in the current bitmap, this method fails. Also, note that this method does not perform format conversion, and will fail if the bitmap formats do not match.

Calling this method may cause the current batch to flush if the bitmap is active in the batch. If the batch that was flushed does not complete successfully, this method fails. However, this method does not clear the error state of the render target on which the batch was flushed. The failing <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> and tag state will be returned at the next call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a>. 

All clips and layers must be popped off of the render target before calling this method.  The method returns <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RENDER_TARGET_HAS_LAYER_OR_CLIPRECT</a>  if any clips or layers are currently applied to the render target.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>

