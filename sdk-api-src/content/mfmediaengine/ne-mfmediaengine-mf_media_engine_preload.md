---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_PRELOAD
title: MF_MEDIA_ENGINE_PRELOAD (mfmediaengine.h)
description: Defines preload hints for the Media Engine.
helpviewer_keywords: ["MF_MEDIA_ENGINE_PRELOAD","MF_MEDIA_ENGINE_PRELOAD enumeration [Media Foundation]","MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC","MF_MEDIA_ENGINE_PRELOAD_EMPTY","MF_MEDIA_ENGINE_PRELOAD_METADATA","MF_MEDIA_ENGINE_PRELOAD_MISSING","MF_MEDIA_ENGINE_PRELOAD_NONE","mf.mf_media_engine_preload","mfmediaengine/MF_MEDIA_ENGINE_PRELOAD","mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC","mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_EMPTY","mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_METADATA","mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_MISSING","mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_NONE"]
old-location: mf\mf_media_engine_preload.htm
tech.root: mf
ms.assetid: 784B3B3F-0A9E-4E34-9197-CE20E2F3FF78
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_PRELOAD, MF_MEDIA_ENGINE_PRELOAD enumeration [Media Foundation], MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC, MF_MEDIA_ENGINE_PRELOAD_EMPTY, MF_MEDIA_ENGINE_PRELOAD_METADATA, MF_MEDIA_ENGINE_PRELOAD_MISSING, MF_MEDIA_ENGINE_PRELOAD_NONE, mf.mf_media_engine_preload, mfmediaengine/MF_MEDIA_ENGINE_PRELOAD, mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC, mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_EMPTY, mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_METADATA, mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_MISSING, mfmediaengine/MF_MEDIA_ENGINE_PRELOAD_NONE
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
req.typenames: MF_MEDIA_ENGINE_PRELOAD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_PRELOAD
 - mfmediaengine/MF_MEDIA_ENGINE_PRELOAD
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
 - MF_MEDIA_ENGINE_PRELOAD
---

# MF_MEDIA_ENGINE_PRELOAD enumeration


## -description

Defines preload hints for the Media Engine. These values correspond to the <b>preload</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -enum-fields

### -field MF_MEDIA_ENGINE_PRELOAD_MISSING:0

The <b>preload</b> attribute is missing.

### -field MF_MEDIA_ENGINE_PRELOAD_EMPTY:1

The <b>preload</b> attribute is an empty string. This value is equivalent to <b>MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC</b>.

### -field MF_MEDIA_ENGINE_PRELOAD_NONE:2

The <b>preload</b> attribute is "none". This value is a hint to the user agent not to preload the resource.

### -field MF_MEDIA_ENGINE_PRELOAD_METADATA:3

The <b>preload</b> attribute is "metadata". This value is a hint to the user agent to fetch the resource metadata.

### -field MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC:4

The <b>preload</b> attribute is "auto". This value is a hint to the user agent to preload the entire resource.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
