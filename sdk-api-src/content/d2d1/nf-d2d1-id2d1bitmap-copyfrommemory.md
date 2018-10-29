---
UID: NF:d2d1.ID2D1Bitmap.CopyFromMemory
title: ID2D1Bitmap::CopyFromMemory
author: windows-sdk-content
description: Copies the specified region from memory into the current bitmap.
old-location: direct2d\ID2D1Bitmap_CopyFromMemory.htm
tech.root: Direct2D
ms.assetid: 594cba56-6f18-439a-ada4-0f591af094bb
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CopyFromMemory, CopyFromMemory method [Direct2D], CopyFromMemory method [Direct2D],ID2D1Bitmap interface, ID2D1Bitmap interface [Direct2D],CopyFromMemory method, ID2D1Bitmap.CopyFromMemory, ID2D1Bitmap::CopyFromMemory, d2d1/ID2D1Bitmap::CopyFromMemory, direct2d.ID2D1Bitmap_CopyFromMemory
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1Bitmap.CopyFromMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Bitmap::CopyFromMemory


## -description


Copies the specified region from memory into the current bitmap.


## -parameters




### -param dstRect [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a>*</b>

In the current bitmap, the upper-left corner of the area to which the region specified by <i>srcRect</i> is copied.


### -param srcData [in]

Type: <b>const void*</b>

The data to copy.


### -param pitch

Type: <b>UINT32</b>

The stride, or pitch, of the source bitmap stored in <i>srcData</i>. The stride is the byte count of a scanline (one row of pixels in memory). The stride can be computed from the following formula: pixel width * bytes per pixel + memory padding.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not update the size of the current bitmap. If the contents of the source bitmap do not fit in the current bitmap, this method fails. Also, note that this method does not perform format conversion; the two bitmap formats should match. 

If this method is passed invalid input (such as an invalid destination rectangle), can produce unpredictable results, such as a distorted image or device failure.

Calling this method may cause the current batch to flush if the bitmap is active in the batch. If the batch that was flushed does not complete successfully, this method fails. However, this method does not clear the error state of the render target on which the batch was flushed. The failing <a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a> and tag state will be returned at the next call to <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a>. 

Starting with Windows 8.1,  this method supports block compressed bitmaps.  If you are using a block compressed format, the end coordinates of the <i>srcRect</i> parameter must be multiples of 4 or the method returns <b>E_INVALIDARG</b>.




## -see-also




<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>
 

 

