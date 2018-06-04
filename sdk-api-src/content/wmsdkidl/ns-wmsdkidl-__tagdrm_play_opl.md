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

# __tagDRM_PLAY_OPL structure


## -description



The <b>DRM_PLAY_OPL</b> structure holds information about the output protection levels (OPL) specified in a license for play actions.




## -struct-fields




### -field minOPL


<a href="https://msdn.microsoft.com/4358c3ea-b65b-4446-b758-c1cd2d68d02a">DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS</a> structure containing the minimum OPL required to play content in different formats.


### -field oplIdReserved

Reserved for future use.


### -field vopi


<a href="https://msdn.microsoft.com/95bce5f8-5230-4b69-b4e9-3cb766edce90">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a> structure containing the video output protection identifiers that apply to playback of the content.


## -see-also




<a href="https://msdn.microsoft.com/cf35626a-5583-440f-8f17-0c9b79bd843d">DRM_COPY_OPL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

