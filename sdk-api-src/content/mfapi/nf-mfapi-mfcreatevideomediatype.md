---
UID: NF:mfapi.MFCreateVideoMediaType
title: MFCreateVideoMediaType function (mfapi.h)
description: Creates a video media type from an MFVIDEOFORMAT structure.
helpviewer_keywords: ["143aedec-d1ce-434a-8a1c-62a2c9d55e88","MFCreateVideoMediaType","MFCreateVideoMediaType function [Media Foundation]","mf.mfcreatevideomediatype","mfapi/MFCreateVideoMediaType"]
old-location: mf\mfcreatevideomediatype.htm
tech.root: mf
ms.assetid: 143aedec-d1ce-434a-8a1c-62a2c9d55e88
ms.date: 12/05/2018
ms.keywords: 143aedec-d1ce-434a-8a1c-62a2c9d55e88, MFCreateVideoMediaType, MFCreateVideoMediaType function [Media Foundation], mf.mfcreatevideomediatype, mfapi/MFCreateVideoMediaType
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
 - MFCreateVideoMediaType
 - mfapi/MFCreateVideoMediaType
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
 - MFCreateVideoMediaType
---

# MFCreateVideoMediaType function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>.]

Creates a video media type from an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -parameters

### -param pVideoFormat [in]

Pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure that describes the video format.

### -param ppIVideoMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Instead of using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure to initialize a video media type, you can call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a> and set the media type attributes directly.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>