---
UID: NF:mfapi.MFCreateVideoMediaTypeFromVideoInfoHeader
title: MFCreateVideoMediaTypeFromVideoInfoHeader function (mfapi.h)
description: Creates a media type from a KS_VIDEOINFOHEADER structure.
helpviewer_keywords: ["922ab0b5-2363-4073-9252-a71b79e03573","MFCreateVideoMediaTypeFromVideoInfoHeader","MFCreateVideoMediaTypeFromVideoInfoHeader function [Media Foundation]","mf.mfcreatevideomediatypefromvideoinfoheader","mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader"]
old-location: mf\mfcreatevideomediatypefromvideoinfoheader.htm
tech.root: mf
ms.assetid: 922ab0b5-2363-4073-9252-a71b79e03573
ms.date: 12/05/2018
ms.keywords: 922ab0b5-2363-4073-9252-a71b79e03573, MFCreateVideoMediaTypeFromVideoInfoHeader, MFCreateVideoMediaTypeFromVideoInfoHeader function [Media Foundation], mf.mfcreatevideomediatypefromvideoinfoheader, mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader
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
 - MFCreateVideoMediaTypeFromVideoInfoHeader
 - mfapi/MFCreateVideoMediaTypeFromVideoInfoHeader
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
 - MFCreateVideoMediaTypeFromVideoInfoHeader
---

# MFCreateVideoMediaTypeFromVideoInfoHeader function


## -description

Creates a media type from a <b>KS_VIDEOINFOHEADER</b> structure.

## -parameters

### -param pVideoInfoHeader

Pointer to the <b>KS_VIDEOINFOHEADER</b> structure to convert. (This structure is identical to the DirectShow <b>VIDEOINFOHEADER</b> structure.)

### -param cbVideoInfoHeader

Size of the <b>KS_VIDEOINFOHEADER</b> structure in bytes.

### -param dwPixelAspectRatioX

The X dimension of the pixel aspect ratio. The pixel aspect ratio is <i>dwPixelAspectRatioX</i>:<i>dwPixelAspectRatioY</i>.

### -param dwPixelAspectRatioY

The Y dimension of the pixel aspect ratio.

### -param InterlaceMode

Member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode">MFVideoInterlaceMode</a> enumeration that specifies how the video is interlaced.

### -param VideoFlags

Bitwise <b>OR</b> of flags from the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoflags">MFVideoFlags</a> enumeration.

### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>KS_VIDEOINFOHEADER</b> structure.

### -param ppIVideoMediaType

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>