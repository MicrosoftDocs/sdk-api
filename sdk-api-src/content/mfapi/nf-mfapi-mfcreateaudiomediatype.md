---
UID: NF:mfapi.MFCreateAudioMediaType
title: MFCreateAudioMediaType function (mfapi.h)
description: Creates an audio media type from a WAVEFORMATEX structure.
helpviewer_keywords: ["8857e150-1746-4f3f-aaa8-db0f44787621","MFCreateAudioMediaType","MFCreateAudioMediaType function [Media Foundation]","mf.mfcreateaudiomediatype","mfapi/MFCreateAudioMediaType"]
old-location: mf\mfcreateaudiomediatype.htm
tech.root: mf
ms.assetid: 8857e150-1746-4f3f-aaa8-db0f44787621
ms.date: 12/05/2018
ms.keywords: 8857e150-1746-4f3f-aaa8-db0f44787621, MFCreateAudioMediaType, MFCreateAudioMediaType function [Media Foundation], mf.mfcreateaudiomediatype, mfapi/MFCreateAudioMediaType
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
 - MFCreateAudioMediaType
 - mfapi/MFCreateAudioMediaType
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
 - MFCreateAudioMediaType
---

# MFCreateAudioMediaType function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future.]

Creates an audio media type from a <b>WAVEFORMATEX</b> structure.

## -parameters

### -param pAudioFormat [in]

Pointer to a <b>WAVEFORMATEX</b> structure that describes the audio format.

### -param ppIAudioMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype">IMFAudioMediaType</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype">IMFAudioMediaType</a> interface is deprecated, so applications should avoid using this function. To create a media type from a <b>WAVEFORMATEX</b> structure, do the following:
      

<ol>
<li>Call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>. This function returns a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The returned media type object is initially empty.
          </li>
<li>Call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex">MFInitMediaTypeFromWaveFormatEx</a> to populate the media type from the <b>WAVEFORMATEX</b> structure.
          </li>
</ol>
Alternatively, you can call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a> and then set the media type attributes directly.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/audio-media-types">Audio Media Types</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>