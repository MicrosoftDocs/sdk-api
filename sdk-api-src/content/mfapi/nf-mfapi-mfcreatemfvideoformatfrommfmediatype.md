---
UID: NF:mfapi.MFCreateMFVideoFormatFromMFMediaType
title: MFCreateMFVideoFormatFromMFMediaType function (mfapi.h)
description: Creates an MFVIDEOFORMAT structure from a video media type.
helpviewer_keywords: ["MFCreateMFVideoFormatFromMFMediaType","MFCreateMFVideoFormatFromMFMediaType function [Media Foundation]","c83e3605-d345-4192-a6fd-26d1a78eb259","mf.mfcreatemfvideoformatfrommfmediatype","mfapi/MFCreateMFVideoFormatFromMFMediaType"]
old-location: mf\mfcreatemfvideoformatfrommfmediatype.htm
tech.root: mf
ms.assetid: c83e3605-d345-4192-a6fd-26d1a78eb259
ms.date: 12/05/2018
ms.keywords: MFCreateMFVideoFormatFromMFMediaType, MFCreateMFVideoFormatFromMFMediaType function [Media Foundation], c83e3605-d345-4192-a6fd-26d1a78eb259, mf.mfcreatemfvideoformatfrommfmediatype, mfapi/MFCreateMFVideoFormatFromMFMediaType
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMFVideoFormatFromMFMediaType
 - mfapi/MFCreateMFVideoFormatFromMFMediaType
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
 - MFCreateMFVideoFormatFromMFMediaType
---

# MFCreateMFVideoFormatFromMFMediaType function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>.]

Creates an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure from a video media type.

## -parameters

### -param pMFType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a video media type.

### -param ppMFVF [out]

Receives a pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure. The caller must release the memory allocated for the structure by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbSize [out]

Receives the size of the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>