---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_CANPLAY
title: MF_MEDIA_ENGINE_CANPLAY (mfmediaengine.h)
description: Specifies the likelihood that the Media Engine can play a specified type of media resource.
helpviewer_keywords: ["MF_MEDIA_ENGINE_CANPLAY","MF_MEDIA_ENGINE_CANPLAY enumeration [Media Foundation]","MF_MEDIA_ENGINE_CANPLAY_MAYBE","MF_MEDIA_ENGINE_CANPLAY_NOT_SUPPORTED","MF_MEDIA_ENGINE_CANPLAY_PROBABLY","mf.mf_media_engine_canplay","mfmediaengine/MF_MEDIA_ENGINE_CANPLAY","mfmediaengine/MF_MEDIA_ENGINE_CANPLAY_MAYBE","mfmediaengine/MF_MEDIA_ENGINE_CANPLAY_NOT_SUPPORTED","mfmediaengine/MF_MEDIA_ENGINE_CANPLAY_PROBABLY"]
old-location: mf\mf_media_engine_canplay.htm
tech.root: mf
ms.assetid: AABABB09-D45F-474C-B692-DC3592ED164F
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_CANPLAY, MF_MEDIA_ENGINE_CANPLAY enumeration [Media Foundation], MF_MEDIA_ENGINE_CANPLAY_MAYBE, MF_MEDIA_ENGINE_CANPLAY_NOT_SUPPORTED, MF_MEDIA_ENGINE_CANPLAY_PROBABLY, mf.mf_media_engine_canplay, mfmediaengine/MF_MEDIA_ENGINE_CANPLAY, mfmediaengine/MF_MEDIA_ENGINE_CANPLAY_MAYBE, mfmediaengine/MF_MEDIA_ENGINE_CANPLAY_NOT_SUPPORTED, mfmediaengine/MF_MEDIA_ENGINE_CANPLAY_PROBABLY
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
req.typenames: MF_MEDIA_ENGINE_CANPLAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_CANPLAY
 - mfmediaengine/MF_MEDIA_ENGINE_CANPLAY
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
 - MF_MEDIA_ENGINE_CANPLAY
---

# MF_MEDIA_ENGINE_CANPLAY enumeration


## -description

Specifies the likelihood that the Media Engine can play a specified type of media resource.

## -enum-fields

### -field MF_MEDIA_ENGINE_CANPLAY_NOT_SUPPORTED:0

The Media Engine cannot play the resource.

### -field MF_MEDIA_ENGINE_CANPLAY_MAYBE:1

The Media Engine might be able to play the resource.

### -field MF_MEDIA_ENGINE_CANPLAY_PROBABLY:2

The Media Engine can probably play the resource.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
