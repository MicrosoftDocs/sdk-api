---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_PROTECTION_FLAGS
title: MF_MEDIA_ENGINE_PROTECTION_FLAGS (mfmediaengine.h)
description: Contains flags that specify whether the Media Engine will play protected content, and whether the Media Engine will use the Protected Media Path (PMP).
helpviewer_keywords: ["MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT","MF_MEDIA_ENGINE_PROTECTION_FLAGS","MF_MEDIA_ENGINE_PROTECTION_FLAGS enumeration [Media Foundation]","MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT","MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP","mf.mf_media_engine_protection_flags","mfmediaengine/MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT","mfmediaengine/MF_MEDIA_ENGINE_PROTECTION_FLAGS","mfmediaengine/MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT","mfmediaengine/MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP"]
old-location: mf\mf_media_engine_protection_flags.htm
tech.root: mf
ms.assetid: 02326325-F122-4D6A-8CA7-3B201378BC15
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT, MF_MEDIA_ENGINE_PROTECTION_FLAGS, MF_MEDIA_ENGINE_PROTECTION_FLAGS enumeration [Media Foundation], MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT, MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP, mf.mf_media_engine_protection_flags, mfmediaengine/MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT, mfmediaengine/MF_MEDIA_ENGINE_PROTECTION_FLAGS, mfmediaengine/MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT, mfmediaengine/MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP
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
req.typenames: MF_MEDIA_ENGINE_PROTECTION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_PROTECTION_FLAGS
 - mfmediaengine/MF_MEDIA_ENGINE_PROTECTION_FLAGS
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
 - MF_MEDIA_ENGINE_PROTECTION_FLAGS
---

# MF_MEDIA_ENGINE_PROTECTION_FLAGS enumeration


## -description

Contains flags that specify whether the Media Engine will play protected content, and whether the Media Engine will use the <a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a> (PMP).

## -enum-fields

### -field MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT:1

Enable playback of protected content. The Media Engine will not play DRM-protected content unless this flag is set. If you set this flag, also set the <a href="/windows/desktop/medfound/mf-media-engine-content-protection-manager">MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER</a> attribute.

### -field MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT:2

Use the <a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a> (PMP) for all playback, including clear (non-protected) content.

### -field MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP:4

Create the PMP inside an unprotected process. You can use this option to play clear content, but not to play protected content.

## -remarks

These flags are used with the <a href="/windows/desktop/medfound/mf-media-engine-content-protection-flags">MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
