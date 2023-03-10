---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_NETWORK
title: MF_MEDIA_ENGINE_NETWORK (mfmediaengine.h)
description: Defines network status codes for the Media Engine.
helpviewer_keywords: ["MF_MEDIA_ENGINE_NETWORK","MF_MEDIA_ENGINE_NETWORK enumeration [Media Foundation]","MF_MEDIA_ENGINE_NETWORK_EMPTY","MF_MEDIA_ENGINE_NETWORK_IDLE","MF_MEDIA_ENGINE_NETWORK_LOADING","MF_MEDIA_ENGINE_NETWORK_NO_SOURCE","mf.mf_media_engine_network","mfmediaengine/MF_MEDIA_ENGINE_NETWORK","mfmediaengine/MF_MEDIA_ENGINE_NETWORK_EMPTY","mfmediaengine/MF_MEDIA_ENGINE_NETWORK_IDLE","mfmediaengine/MF_MEDIA_ENGINE_NETWORK_LOADING","mfmediaengine/MF_MEDIA_ENGINE_NETWORK_NO_SOURCE"]
old-location: mf\mf_media_engine_network.htm
tech.root: mf
ms.assetid: A2A73A54-C360-452C-8887-D3065274358A
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_NETWORK, MF_MEDIA_ENGINE_NETWORK enumeration [Media Foundation], MF_MEDIA_ENGINE_NETWORK_EMPTY, MF_MEDIA_ENGINE_NETWORK_IDLE, MF_MEDIA_ENGINE_NETWORK_LOADING, MF_MEDIA_ENGINE_NETWORK_NO_SOURCE, mf.mf_media_engine_network, mfmediaengine/MF_MEDIA_ENGINE_NETWORK, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_EMPTY, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_IDLE, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_LOADING, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_NO_SOURCE
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
req.typenames: MF_MEDIA_ENGINE_NETWORK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_NETWORK
 - mfmediaengine/MF_MEDIA_ENGINE_NETWORK
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
 - MF_MEDIA_ENGINE_NETWORK
---

# MF_MEDIA_ENGINE_NETWORK enumeration


## -description

Defines network status codes for the Media Engine.

## -enum-fields

### -field MF_MEDIA_ENGINE_NETWORK_EMPTY:0

The initial state.

### -field MF_MEDIA_ENGINE_NETWORK_IDLE:1

The Media Engine has started the resource selection algorithm, and has selected a media resource, but is not using the network.

### -field MF_MEDIA_ENGINE_NETWORK_LOADING:2

The Media Engine is loading a media resource.

### -field MF_MEDIA_ENGINE_NETWORK_NO_SOURCE:3

The Media Engine has started the resource selection algorithm, but has not selected a media resource.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getnetworkstate">IMFMediaEngine::GetNetworkState</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
