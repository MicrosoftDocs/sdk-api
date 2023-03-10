---
UID: NF:mfapi.MFGetUncompressedVideoFormat
title: MFGetUncompressedVideoFormat function (mfapi.h)
description: Returns the FOURCC or D3DFORMAT value for an uncompressed video format.
helpviewer_keywords: ["7869025a-dacf-47e6-b129-db5b2daefa3b","MFGetUncompressedVideoFormat","MFGetUncompressedVideoFormat function [Media Foundation]","mf.mfgetuncompressedvideoformat","mfapi/MFGetUncompressedVideoFormat"]
old-location: mf\mfgetuncompressedvideoformat.htm
tech.root: mf
ms.assetid: 7869025a-dacf-47e6-b129-db5b2daefa3b
ms.date: 12/05/2018
ms.keywords: 7869025a-dacf-47e6-b129-db5b2daefa3b, MFGetUncompressedVideoFormat, MFGetUncompressedVideoFormat function [Media Foundation], mf.mfgetuncompressedvideoformat, mfapi/MFGetUncompressedVideoFormat
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
 - MFGetUncompressedVideoFormat
 - mfapi/MFGetUncompressedVideoFormat
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
 - MFGetUncompressedVideoFormat
---

# MFGetUncompressedVideoFormat function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>.]

Returns the FOURCC or <b>D3DFORMAT</b> value for an uncompressed video format.

## -parameters

### -param pVideoFormat [in]

Pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -returns

Returns a FOURCC or <b>D3DFORMAT</b> value that identifies the video format. If the video format is compressed or not recognized, the return value is D3DFMT_UNKNOWN.

## -remarks

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>