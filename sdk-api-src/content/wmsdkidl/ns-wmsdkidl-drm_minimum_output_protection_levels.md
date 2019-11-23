---
UID: NS:wmsdkidl.__tagDRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmsdkidl.h)

description: The DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS structure holds the minimum output protection levels (OPL) for playback of various types of content. A device must support the minimum OPL for a type of data to receive that type of data from the reader.
old-location: wmformat\drm_minimum_output_protection_levels.htm
tech.root: wmformat
ms.assetid: 4358c3ea-b65b-4446-b758-c1cd2d68d02a

ms.date: 12/05/2018
ms.keywords: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS, DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS structure [windows Media Format], structure [windows Media Format], wmformat.drm_minimum_output_protection_levels, wmsdkidl/DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
ms.topic: struct
f1_keywords: 
 - "wmsdkidl/DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
req.redist: 
ms.custom: 19H1
---

# DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS structure


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



This structure is used as a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl">DRM_PLAY_OPL</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/structures">Structures</a>
 

 

