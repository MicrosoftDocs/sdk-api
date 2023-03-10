---
UID: NF:mfapi.MFInitMediaTypeFromVideoInfoHeader
title: MFInitMediaTypeFromVideoInfoHeader function (mfapi.h)
description: Initializes a media type from a DirectShow VIDEOINFOHEADER structure.
helpviewer_keywords: ["7f88422d-c968-4eea-83cb-45e6cfe37921","MFInitMediaTypeFromVideoInfoHeader","MFInitMediaTypeFromVideoInfoHeader function [Media Foundation]","mf.mfinitmediatypefromvideoinfoheader","mfapi/MFInitMediaTypeFromVideoInfoHeader"]
old-location: mf\mfinitmediatypefromvideoinfoheader.htm
tech.root: mf
ms.assetid: 7f88422d-c968-4eea-83cb-45e6cfe37921
ms.date: 12/05/2018
ms.keywords: 7f88422d-c968-4eea-83cb-45e6cfe37921, MFInitMediaTypeFromVideoInfoHeader, MFInitMediaTypeFromVideoInfoHeader function [Media Foundation], mf.mfinitmediatypefromvideoinfoheader, mfapi/MFInitMediaTypeFromVideoInfoHeader
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
 - MFInitMediaTypeFromVideoInfoHeader
 - mfapi/MFInitMediaTypeFromVideoInfoHeader
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
 - MFInitMediaTypeFromVideoInfoHeader
---

# MFInitMediaTypeFromVideoInfoHeader function


## -description

Initializes a media type from a DirectShow <b>VIDEOINFOHEADER</b> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.

### -param pVIH

Pointer to a <b>VIDEOINFOHEADER</b> structure that describes the media type. The caller must fill in the structure members before calling this function.

### -param cbBufSize

Size of the <b>VIDEOINFOHEADER</b> structure, in bytes.

### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>VIDEOINFOHEADER</b> structure.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>