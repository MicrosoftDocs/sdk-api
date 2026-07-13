---
UID: NF:mfapi.MFGetStrideForBitmapInfoHeader
title: MFGetStrideForBitmapInfoHeader function (mfapi.h)
description: Calculates the minimum surface stride for a video format.
helpviewer_keywords: ["09612b83-8b14-4286-9562-9e3d00fe2c2b","MFGetStrideForBitmapInfoHeader","MFGetStrideForBitmapInfoHeader function [Media Foundation]","mf.mfgetstrideforbitmapinfoheader","mfapi/MFGetStrideForBitmapInfoHeader"]
old-location: mf\mfgetstrideforbitmapinfoheader.htm
tech.root: mf
ms.assetid: 09612b83-8b14-4286-9562-9e3d00fe2c2b
ms.date: 12/05/2018
ms.keywords: 09612b83-8b14-4286-9562-9e3d00fe2c2b, MFGetStrideForBitmapInfoHeader, MFGetStrideForBitmapInfoHeader function [Media Foundation], mf.mfgetstrideforbitmapinfoheader, mfapi/MFGetStrideForBitmapInfoHeader
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetStrideForBitmapInfoHeader
 - mfapi/MFGetStrideForBitmapInfoHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetStrideForBitmapInfoHeader
---

# MFGetStrideForBitmapInfoHeader function


## -description

Calculates the minimum surface stride for a video format.

## -parameters

### -param format [in]

FOURCC code or <b>D3DFORMAT</b> value that specifies the video format. If you have a video subtype GUID, you can use the first <b>DWORD</b> of the subtype.

### -param dwWidth [in]

Width of the image, in pixels.

### -param pStride [out]

Receives the minimum surface stride, in pixels.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function calculates the minimum stride needed to hold the image in memory. Use this function if you are allocating buffers in system memory. Surfaces allocated in video memory might require a larger stride, depending on the graphics card.
      

If you are working with a DirectX surface buffer, use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">IMF2DBuffer::Lock2D</a> method to find the surface stride.
      

For planar YUV formats, this function returns the stride for the Y plane. Depending on the format, the chroma planes might have a different stride.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/image-stride">Image Stride</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>