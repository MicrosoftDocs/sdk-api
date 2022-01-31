---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_CREATEFLAGS
title: MF_MEDIA_ENGINE_CREATEFLAGS (mfmediaengine.h)
description: Contains flags for the IMFMediaEngineClassFactory::CreateInstance method.
helpviewer_keywords: ["MF_MEDIA_ENGINE_AUDIOONLY","MF_MEDIA_ENGINE_CREATEFLAGS","MF_MEDIA_ENGINE_CREATEFLAGS enumeration [Media Foundation]","MF_MEDIA_ENGINE_CREATEFLAGS_MASK","MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS","MF_MEDIA_ENGINE_FORCEMUTE","MF_MEDIA_ENGINE_REAL_TIME_MODE","MF_MEDIA_ENGINE_WAITFORSTABLE_STATE","mf.mf_media_engine_createflags","mfmediaengine/MF_MEDIA_ENGINE_AUDIOONLY","mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS","mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS_MASK","mfmediaengine/MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS","mfmediaengine/MF_MEDIA_ENGINE_FORCEMUTE","mfmediaengine/MF_MEDIA_ENGINE_REAL_TIME_MODE","mfmediaengine/MF_MEDIA_ENGINE_WAITFORSTABLE_STATE"]
old-location: mf\mf_media_engine_createflags.htm
tech.root: mf
ms.assetid: 1709B08C-D4DC-4A33-9B92-1C4961208684
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_AUDIOONLY, MF_MEDIA_ENGINE_CREATEFLAGS, MF_MEDIA_ENGINE_CREATEFLAGS enumeration [Media Foundation], MF_MEDIA_ENGINE_CREATEFLAGS_MASK, MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS, MF_MEDIA_ENGINE_FORCEMUTE, MF_MEDIA_ENGINE_REAL_TIME_MODE, MF_MEDIA_ENGINE_WAITFORSTABLE_STATE, mf.mf_media_engine_createflags, mfmediaengine/MF_MEDIA_ENGINE_AUDIOONLY, mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS, mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS_MASK, mfmediaengine/MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS, mfmediaengine/MF_MEDIA_ENGINE_FORCEMUTE, mfmediaengine/MF_MEDIA_ENGINE_REAL_TIME_MODE, mfmediaengine/MF_MEDIA_ENGINE_WAITFORSTABLE_STATE
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
req.typenames: MF_MEDIA_ENGINE_CREATEFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_CREATEFLAGS
 - mfmediaengine/MF_MEDIA_ENGINE_CREATEFLAGS
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
 - MF_MEDIA_ENGINE_CREATEFLAGS
---

# MF_MEDIA_ENGINE_CREATEFLAGS enumeration


## -description

Contains flags for the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">IMFMediaEngineClassFactory::CreateInstance</a>  method.

## -enum-fields

### -field MF_MEDIA_ENGINE_AUDIOONLY:0x1

The Media Engine will play audio only. It will not play video.

### -field MF_MEDIA_ENGINE_WAITFORSTABLE_STATE:0x2

The Media Engine's resource loading algorithm waits for the application to signal the thread that loads the resource. For more information, see the remarks for <b>MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE</b> in the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_event">MF_MEDIA_ENGINE_EVENT</a> enumeration.

### -field MF_MEDIA_ENGINE_FORCEMUTE:0x4

Always mute the audio.

### -field MF_MEDIA_ENGINE_REAL_TIME_MODE:0x8

Enable low-latency mode in the rendering pipeline. This can be changed at a later time by calling <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setrealtimemode">IMFMediaEngineEx::SetRealTimeMode</a>.

### -field MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS:0x10

Disable locally registered media plugins. If this flag is set, the Media Engine will not load decoders or other media plugins that the application registered for the local process.

### -field MF_MEDIA_ENGINE_CREATEFLAGS_MASK:0x1f

Reserved.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
