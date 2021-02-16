---
UID: NF:mfobjects.IMF2DBuffer.GetScanline0AndPitch
title: IMF2DBuffer::GetScanline0AndPitch (mfobjects.h)
description: Retrieves a pointer to the buffer memory and the surface stride.
helpviewer_keywords: ["08a5f659-609d-4a86-a24e-b30bb7f9e835","GetScanline0AndPitch","GetScanline0AndPitch method [Media Foundation]","GetScanline0AndPitch method [Media Foundation]","IMF2DBuffer interface","IMF2DBuffer interface [Media Foundation]","GetScanline0AndPitch method","IMF2DBuffer.GetScanline0AndPitch","IMF2DBuffer::GetScanline0AndPitch","mf.imf2dbuffer_getscanline0andpitch","mfobjects/IMF2DBuffer::GetScanline0AndPitch"]
old-location: mf\imf2dbuffer_getscanline0andpitch.htm
tech.root: mf
ms.assetid: 08a5f659-609d-4a86-a24e-b30bb7f9e835
ms.date: 12/05/2018
ms.keywords: 08a5f659-609d-4a86-a24e-b30bb7f9e835, GetScanline0AndPitch, GetScanline0AndPitch method [Media Foundation], GetScanline0AndPitch method [Media Foundation],IMF2DBuffer interface, IMF2DBuffer interface [Media Foundation],GetScanline0AndPitch method, IMF2DBuffer.GetScanline0AndPitch, IMF2DBuffer::GetScanline0AndPitch, mf.imf2dbuffer_getscanline0andpitch, mfobjects/IMF2DBuffer::GetScanline0AndPitch
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
 - IMF2DBuffer::GetScanline0AndPitch
 - mfobjects/IMF2DBuffer::GetScanline0AndPitch
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
 - IMF2DBuffer.GetScanline0AndPitch
---

# IMF2DBuffer::GetScanline0AndPitch


## -description

Retrieves a pointer to the buffer memory and the surface stride.

## -parameters

### -param pbScanline0 [out]

Receives a pointer to the first byte of the top row of pixels in the image.

### -param plPitch [out]

Receives the stride, in bytes. For more information, see <a href="/windows/desktop/medfound/image-stride">Image Stride</a>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
You must lock the buffer before calling this method.

</td>
</tr>
</table>

## -remarks

Before calling this method, you must lock the buffer by calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">IMF2DBuffer::Lock2D</a>. The pointer returned in <i>plPitch</i> is valid only while the buffer remains locked.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>