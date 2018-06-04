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

# MF_MEDIA_ENGINE_PRELOAD enumeration


## -description


Defines preload hints for the Media Engine. These values correspond to the <b>preload</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.


## -enum-fields




### -field MF_MEDIA_ENGINE_PRELOAD_MISSING

The <b>preload</b> attribute is missing. 


### -field MF_MEDIA_ENGINE_PRELOAD_EMPTY

The <b>preload</b> attribute is an empty string. This value is equivalent to <b>MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC</b>.


### -field MF_MEDIA_ENGINE_PRELOAD_NONE

The <b>preload</b> attribute is "none". This value is a hint to the user agent not to preload the resource.


### -field MF_MEDIA_ENGINE_PRELOAD_METADATA

The <b>preload</b> attribute is "metadata". This value is a hint to the user agent to fetch the resource metadata.


### -field MF_MEDIA_ENGINE_PRELOAD_AUTOMATIC

The <b>preload</b> attribute is "auto". This value is a hint to the user agent to preload the entire resource.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

