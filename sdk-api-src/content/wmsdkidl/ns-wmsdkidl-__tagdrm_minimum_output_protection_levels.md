---
UID: NS:wmsdkidl.__tagDRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
title: "__tagDRM_MINIMUM_OUTPUT_PROTECTION_LEVELS"
author: windows-sdk-content
description: The DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS structure holds the minimum output protection levels (OPL) for playback of various types of content. A device must support the minimum OPL for a type of data to receive that type of data from the reader.
old-location: wmformat\drm_minimum_output_protection_levels.htm
tech.root: wmformat
ms.assetid: 4358c3ea-b65b-4446-b758-c1cd2d68d02a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS, DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS structure [windows Media Format], __tagDRM_MINIMUM_OUTPUT_PROTECTION_LEVELS, structure [windows Media Format], wmformat.drm_minimum_output_protection_levels, wmsdkidl/DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Drmexternals.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - wmsdkidl.h
api_name:
 - DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
product: Windows
targetos: Windows
req.typenames: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
req.redist: 
---

# __tagDRM_MINIMUM_OUTPUT_PROTECTION_LEVELS structure


## -description



The <b>DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS</b> structure holds the minimum output protection levels (OPL) for playback of various types of content. A device must support the minimum OPL for a type of data to receive that type of data from the reader.




## -struct-fields




### -field wCompressedDigitalVideo

Minimum OPL required to receive compressed digital video.


### -field wUncompressedDigitalVideo

Minimum OPL required to receive uncompressed digital video.


### -field wAnalogVideo

Minimum OPL required to receive analog video.


### -field wCompressedDigitalAudio

Minimum OPL required to receive compressed digital audio.


### -field wUncompressedDigitalAudio

Minimum OPL required to receive uncompressed digital audio.


## -remarks



This structure is used as a member of the <a href="https://msdn.microsoft.com/5d14bd02-0fb5-4982-b3dc-7f8277cb852f">DRM_PLAY_OPL</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

