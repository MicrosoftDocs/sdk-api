---
UID: NF:mfapi.MFInitMediaTypeFromMFVideoFormat
title: MFInitMediaTypeFromMFVideoFormat function (mfapi.h)
description: Initializes a media type from an MFVIDEOFORMAT structure.
helpviewer_keywords: ["45400b67-df81-4fae-a24d-80020eb07151","MFInitMediaTypeFromMFVideoFormat","MFInitMediaTypeFromMFVideoFormat function [Media Foundation]","mf.mfinitmediatypefrommfvideoformat","mfapi/MFInitMediaTypeFromMFVideoFormat"]
old-location: mf\mfinitmediatypefrommfvideoformat.htm
tech.root: mf
ms.assetid: 45400b67-df81-4fae-a24d-80020eb07151
ms.date: 12/05/2018
ms.keywords: 45400b67-df81-4fae-a24d-80020eb07151, MFInitMediaTypeFromMFVideoFormat, MFInitMediaTypeFromMFVideoFormat function [Media Foundation], mf.mfinitmediatypefrommfvideoformat, mfapi/MFInitMediaTypeFromMFVideoFormat
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
 - MFInitMediaTypeFromMFVideoFormat
 - mfapi/MFInitMediaTypeFromMFVideoFormat
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
 - MFInitMediaTypeFromMFVideoFormat
---

# MFInitMediaTypeFromMFVideoFormat function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>.]

Initializes a media type from an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.

### -param pMFVF

Pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure that describes the media type. The caller must fill in the structure members before calling this function.

### -param cbBufSize

Size of the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, in bytes.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>