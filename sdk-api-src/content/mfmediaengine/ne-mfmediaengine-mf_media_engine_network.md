---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_NETWORK
title: MF_MEDIA_ENGINE_NETWORK
author: windows-sdk-content
description: Defines network status codes for the Media Engine.
old-location: mf\mf_media_engine_network.htm
tech.root: medfound
ms.assetid: A2A73A54-C360-452C-8887-D3065274358A
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MF_MEDIA_ENGINE_NETWORK, MF_MEDIA_ENGINE_NETWORK enumeration [Media Foundation], MF_MEDIA_ENGINE_NETWORK_EMPTY, MF_MEDIA_ENGINE_NETWORK_IDLE, MF_MEDIA_ENGINE_NETWORK_LOADING, MF_MEDIA_ENGINE_NETWORK_NO_SOURCE, mf.mf_media_engine_network, mfmediaengine/MF_MEDIA_ENGINE_NETWORK, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_EMPTY, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_IDLE, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_LOADING, mfmediaengine/MF_MEDIA_ENGINE_NETWORK_NO_SOURCE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_NETWORK
product: Windows
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_NETWORK
req.redist: 
---

# MF_MEDIA_ENGINE_NETWORK enumeration


## -description


Defines network status codes for the Media Engine.


## -enum-fields




### -field MF_MEDIA_ENGINE_NETWORK_EMPTY

The initial state.


### -field MF_MEDIA_ENGINE_NETWORK_IDLE

The Media Engine has started the resource selection algorithm, and has selected a media resource, but is not using the network.


### -field MF_MEDIA_ENGINE_NETWORK_LOADING

The Media Engine is loading a media resource.


### -field MF_MEDIA_ENGINE_NETWORK_NO_SOURCE

The Media Engine has started the resource selection algorithm, but has not selected a media resource.


## -see-also




<a href="https://msdn.microsoft.com/7CCA902A-51E9-4B6D-B16C-643177BE1BC9">IMFMediaEngine::GetNetworkState</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

