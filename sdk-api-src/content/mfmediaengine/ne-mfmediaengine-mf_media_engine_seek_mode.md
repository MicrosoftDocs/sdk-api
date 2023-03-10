---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_SEEK_MODE
title: MF_MEDIA_ENGINE_SEEK_MODE (mfmediaengine.h)
description: Defines values for the media engine seek mode.
helpviewer_keywords: ["MF_MEDIA_ENGINE_SEEK_MODE","MF_MEDIA_ENGINE_SEEK_MODE enumeration [Media Foundation]","MF_MEDIA_ENGINE_SEEK_MODE_APPROXIMATE","MF_MEDIA_ENGINE_SEEK_MODE_NORMAL","mf.mf_media_engine_seek_mode","mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE","mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE_APPROXIMATE","mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE_NORMAL"]
old-location: mf\mf_media_engine_seek_mode.htm
tech.root: mf
ms.assetid: 58356FC2-5F1E-463F-98D5-E63AFCC05A02
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_SEEK_MODE, MF_MEDIA_ENGINE_SEEK_MODE enumeration [Media Foundation], MF_MEDIA_ENGINE_SEEK_MODE_APPROXIMATE, MF_MEDIA_ENGINE_SEEK_MODE_NORMAL, mf.mf_media_engine_seek_mode, mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE, mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE_APPROXIMATE, mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE_NORMAL
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_SEEK_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_SEEK_MODE
 - mfmediaengine/MF_MEDIA_ENGINE_SEEK_MODE
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
 - MF_MEDIA_ENGINE_SEEK_MODE
---

# MF_MEDIA_ENGINE_SEEK_MODE enumeration


## -description

Defines values for the media engine seek mode.

## -enum-fields

### -field MF_MEDIA_ENGINE_SEEK_MODE_NORMAL:0

Specifies normal seek.

### -field MF_MEDIA_ENGINE_SEEK_MODE_APPROXIMATE:1

Specifies an approximate seek.

## -remarks

This enumeration is used with the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setcurrenttimeex">MediaEngineEx::SetCurrentTimeEx</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
