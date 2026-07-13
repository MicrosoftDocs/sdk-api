---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
title: MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS (mfmediaengine.h)
description: Specifies the content protection requirements for a video frame.
helpviewer_keywords: ["MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS","MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS enumeration [Media Foundation]","MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED","MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION","MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION","mf.mf_media_engine_frame_protection_flags","mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS","mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED","mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION","mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION"]
old-location: mf\mf_media_engine_frame_protection_flags.htm
tech.root: mf
ms.assetid: 6864ED4B-BB75-4176-992B-ABC95B81001A
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS, MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS enumeration [Media Foundation], MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED, MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION, MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION, mf.mf_media_engine_frame_protection_flags, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
 - mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
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
 - MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
---

# MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS enumeration


## -description

Specifies the content protection requirements for a video frame.

## -enum-fields

### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED:0x1

The video frame should be protected.

### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION:0x2

Direct3D surface protection must be applied to any surface that contains the frame.

### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION:0x4

Direct3D anti-screen-scrape protection must be applied to any surface that contains the frame.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-getrequiredprotections">IMFMediaEngineProtectedContent::GetRequiredProtections</a>



<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-transfervideoframe">IMFMediaEngineProtectedContent::TransferVideoFrame</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
