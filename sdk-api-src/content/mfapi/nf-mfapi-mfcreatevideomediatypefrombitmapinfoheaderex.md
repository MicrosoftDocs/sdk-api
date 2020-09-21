---
UID: NF:mfapi.MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
title: MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function (mfapi.h)
description: Creates a video media type from a BITMAPINFOHEADER structure.
helpviewer_keywords: ["MFCreateVideoMediaTypeFromBitMapInfoHeaderEx","MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function [Media Foundation]","mf.mfcreatevideomediatypefrombitmapinfoheaderex","mfapi/MFCreateVideoMediaTypeFromBitMapInfoHeaderEx"]
old-location: mf\mfcreatevideomediatypefrombitmapinfoheaderex.htm
tech.root: mf
ms.assetid: 27160995-e934-4050-a231-d69d4f75dfce
ms.date: 12/05/2018
ms.keywords: MFCreateVideoMediaTypeFromBitMapInfoHeaderEx, MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function [Media Foundation], mf.mfcreatevideomediatypefrombitmapinfoheaderex, mfapi/MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
 - mfapi/MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
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
 - MFCreateVideoMediaTypeFromBitMapInfoHeaderEx
---

# MFCreateVideoMediaTypeFromBitMapInfoHeaderEx function


## -description

Creates a video media type from a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

## -parameters

### -param pbmihBitMapInfoHeader [in]

A pointer to the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure to convert.

### -param cbBitMapInfoHeader [in]

The size of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure in bytes, including the size of any palette entries or color masks that follow the structure.

### -param dwPixelAspectRatioX

The X dimension of the pixel aspect ratio.

### -param dwPixelAspectRatioY

The Y dimension of the pixel aspect ratio.

### -param InterlaceMode

A member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode">MFVideoInterlaceMode</a> enumeration, specifying how the video is interlaced.

### -param VideoFlags

A bitwise <b>OR</b> of flags from the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoflags">MFVideoFlags</a> enumeration.

### -param dwFramesPerSecondNumerator

The numerator of the 
          frame rate in frames per second.

### -param dwFramesPerSecondDenominator

The denominator of the frame rate in frames per second

### -param dwMaxBitRate

The approximate data rate of the video stream, in bits per second. If the rate is unknown, set this parameter to zero.

### -param ppIVideoMediaType [out]

Receives a pointer to the 
          <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a> interface. The caller must release the interface.

## -returns

If the function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>