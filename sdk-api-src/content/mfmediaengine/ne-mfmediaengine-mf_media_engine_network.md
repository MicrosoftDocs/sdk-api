---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

