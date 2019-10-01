---
UID: NN:wincodec.IWICBitmapLock
title: IWICBitmapLock (wincodec.h)
author: windows-sdk-content
description: Exposes methods that support the Lock method.
old-location: wic\_wic_codec_iwicbitmaplock.htm
tech.root: wic
ms.assetid: c0ddbc25-6abe-484b-a545-3b9376c514df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICBitmapLock, IWICBitmapLock interface [Windows Imaging Component], IWICBitmapLock interface [Windows Imaging Component],described, _wic_codec_iwicbitmaplock, wic._wic_codec_iwicbitmaplock, wincodec/IWICBitmapLock
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICBitmapLock"
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapLock interface


## -description


Exposes methods that support the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapLock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmaplock-getdatapointer">GetDataPointer</a>
</td>
<td align="left" width="63%">
Gets the pointer to the top left pixel in the locked rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmaplock-getpixelformat">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Gets the pixel format of for the locked area of pixels. This can be used to compute the number of bytes-per-pixel in the locked area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmaplock-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the width and height, in pixels, of the locked rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmaplock-getstride">GetStride</a>
</td>
<td align="left" width="63%">
Provides access to the <a href="https://docs.microsoft.com/">stride</a> value for the memory.

</td>
</tr>
</table> 


## -remarks



The bitmap lock is simply an abstraction for a rectangular memory window into the bitmap. For the simplest case, a system memory bitmap, this is simply a pointer to the top left corner of the rectangle and a stride value.

To release the exclusive lock set by <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a> method and the associated <b>IWICBitmapLock</b> object, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the <b>IWICBitmapLock</b> object.



