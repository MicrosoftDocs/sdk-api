---
UID: NN:mfobjects.IMF2DBuffer
title: IMF2DBuffer (mfobjects.h)
description: Represents a buffer that contains a two-dimensional surface, such as a video frame. (IMF2DBuffer)
helpviewer_keywords: ["80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7","IMF2DBuffer","IMF2DBuffer interface [Media Foundation]","IMF2DBuffer interface [Media Foundation]","described","mf.imf2dbuffer","mfobjects/IMF2DBuffer"]
old-location: mf\imf2dbuffer.htm
tech.root: mf
ms.assetid: 80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7
ms.date: 12/05/2018
ms.keywords: 80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7, IMF2DBuffer, IMF2DBuffer interface [Media Foundation], IMF2DBuffer interface [Media Foundation],described, mf.imf2dbuffer, mfobjects/IMF2DBuffer
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMF2DBuffer
 - mfobjects/IMF2DBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMF2DBuffer
---

# IMF2DBuffer interface


## -description

Represents a buffer that contains a two-dimensional surface, such as a video frame.

## -inheritance

The <b>IMF2DBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMF2DBuffer</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <b>QueryInterface</b> on the media buffer.

To use a 2-D buffer, it is important to know the <i>stride</i>, which is the number of bytes needed to go from one row of pixels to the next. The stride may be larger than the image width, because the surface may contain padding bytes after each row of pixels. Stride can also be negative, if the pixels are oriented bottom-up in memory. For more information, see <a href="/windows/desktop/medfound/image-stride">Image Stride</a>.

Every video format defines a <i>contiguous</i> or <i>packed</i> representation. This representation is compatible with the standard layout of a DirectX surface in system memory, with no additional padding. For RGB video, the contiguous representation has a pitch equal to the image width in bytes, rounded up to the nearest <b>DWORD</b> boundary. For YUV video, the layout of the contiguous representation depends on the YUV format. For planar YUV formats, the Y plane might have a different pitch than the U and V planes.

If a media buffer supports the <b>IMF2DBuffer</b> interface, the underlying buffer is not guaranteed to have a contiguous representation, because there might be additional padding bytes after each row of pixels. When a buffer is non-contiguous, the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">Lock</a> and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">Lock2D</a> methods have different behaviors:

<ul>
<li>The <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">Lock2D</a> method returns a pointer to the underlying buffer. The buffer might not be contiguous.
          </li>
<li>The <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">Lock</a> method returns a buffer that is guaranteed to be contiguous. If the underlying buffer is not contiguous, the method copies the data into a new buffer, and the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">Unlock</a> method copies it back into the original buffer.
          </li>
</ul>
Call the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">Lock2D</a> method to access the 2-D buffer in its native format. The native format might not be contiguous. The buffer's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">IMFMediaBuffer::Lock</a> method returns a contiguous representation of the buffer. However, this might require an internal copy from the native format. For 2-D buffers, therefore, you should use the <b>Lock2D</b> method and avoid the <b>Lock</b> method. Because the <b>Lock</b> method might cause up to two buffer copies, the <b>Lock2D</b> method is generally more efficient and should be used when possible. To find out if the underlying buffer is contiguous, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-iscontiguousformat">IMF2DBuffer::IsContiguousFormat</a>.

For uncompressed images, the amount of valid data in the buffer is determined by the width, height, and pixel layout of the image. For this reason, if you call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">Lock2D</a> to access the buffer, do not rely on the values returned by <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">IMFMediaBuffer::GetCurrentLength</a> or <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength">IMFMediaBuffer::GetMaxLength</a>. Similarly, if you modify the data in the buffer, you do not have to call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength">IMFMediaBuffer::SetCurrentLength</a> to update the size. Generally, you should avoid mixing calls to <b>IMF2DBuffer</b> and <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> methods on the same media buffer.

## -see-also

<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>
