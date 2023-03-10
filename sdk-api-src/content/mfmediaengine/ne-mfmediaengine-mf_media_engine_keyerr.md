---
UID: NE:mfmediaengine._MF_MEDIA_ENGINE_KEYERR
title: MF_MEDIA_ENGINE_KEYERR (mfmediaengine.h)
description: Defines media key error codes for the media engine.
helpviewer_keywords: ["MF_MEDIAENGINE_KEYERR_CLIENT","MF_MEDIAENGINE_KEYERR_DOMAIN","MF_MEDIAENGINE_KEYERR_HARDWARECHANGE","MF_MEDIAENGINE_KEYERR_OUTPUT","MF_MEDIAENGINE_KEYERR_SERVICE","MF_MEDIAENGINE_KEYERR_UNKNOWN","MF_MEDIA_ENGINE_KEYERR","MF_MEDIA_ENGINE_KEYERR enumeration [Media Foundation]","mf.mf_media_engine_keyerr","mfmediaengine/MF_MEDIAENGINE_KEYERR_CLIENT","mfmediaengine/MF_MEDIAENGINE_KEYERR_DOMAIN","mfmediaengine/MF_MEDIAENGINE_KEYERR_HARDWARECHANGE","mfmediaengine/MF_MEDIAENGINE_KEYERR_OUTPUT","mfmediaengine/MF_MEDIAENGINE_KEYERR_SERVICE","mfmediaengine/MF_MEDIAENGINE_KEYERR_UNKNOWN","mfmediaengine/MF_MEDIA_ENGINE_KEYERR"]
old-location: mf\mf_media_engine_keyerr.htm
tech.root: mf
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
ms.date: 12/05/2018
ms.keywords: MF_MEDIAENGINE_KEYERR_CLIENT, MF_MEDIAENGINE_KEYERR_DOMAIN, MF_MEDIAENGINE_KEYERR_HARDWARECHANGE, MF_MEDIAENGINE_KEYERR_OUTPUT, MF_MEDIAENGINE_KEYERR_SERVICE, MF_MEDIAENGINE_KEYERR_UNKNOWN, MF_MEDIA_ENGINE_KEYERR, MF_MEDIA_ENGINE_KEYERR enumeration [Media Foundation], mf.mf_media_engine_keyerr, mfmediaengine/MF_MEDIAENGINE_KEYERR_CLIENT, mfmediaengine/MF_MEDIAENGINE_KEYERR_DOMAIN, mfmediaengine/MF_MEDIAENGINE_KEYERR_HARDWARECHANGE, mfmediaengine/MF_MEDIAENGINE_KEYERR_OUTPUT, mfmediaengine/MF_MEDIAENGINE_KEYERR_SERVICE, mfmediaengine/MF_MEDIAENGINE_KEYERR_UNKNOWN, mfmediaengine/MF_MEDIA_ENGINE_KEYERR
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_KEYERR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_MEDIA_ENGINE_KEYERR
 - mfmediaengine/_MF_MEDIA_ENGINE_KEYERR
 - MF_MEDIA_ENGINE_KEYERR
 - mfmediaengine/MF_MEDIA_ENGINE_KEYERR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_KEYERR
---

# MF_MEDIA_ENGINE_KEYERR enumeration


## -description

Defines media key error codes for the media engine.

## -enum-fields

### -field MF_MEDIAENGINE_KEYERR_UNKNOWN:1

Unknown error occurred.

### -field MF_MEDIAENGINE_KEYERR_CLIENT:2

An error with the client occurred.

### -field MF_MEDIAENGINE_KEYERR_SERVICE:3

An error with the service occurred.

### -field MF_MEDIAENGINE_KEYERR_OUTPUT:4

An error with the output occurred.

### -field MF_MEDIAENGINE_KEYERR_HARDWARECHANGE:5

An error occurred related to a hardware change.

### -field MF_MEDIAENGINE_KEYERR_DOMAIN:6

An error with the domain occurred.

## -remarks

<b>MF_MEDIA_ENGINE_KEYERR</b> is used with the <i>code</i> parameter of  <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror">IMFMediaKeySessionNotify::KeyError</a> and the <i>code</i> value returned from <a href="/windows/desktop/medfound/imfmediakeysession-geterror">IMFMediaKeySession::GetError</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
