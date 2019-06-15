---
UID: NS:wmsdkidl.__tagDRM_PLAY_OPL
title: DRM_PLAY_OPL (wmsdkidl.h)
author: windows-sdk-content
description: The DRM_PLAY_OPL structure holds information about the output protection levels (OPL) specified in a license for play actions.
old-location: wmformat\drm_play_opl.htm
tech.root: wmformat
ms.assetid: 5d14bd02-0fb5-4982-b3dc-7f8277cb852f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRM_PLAY_OPL, DRM_PLAY_OPL structure [windows Media Format], structure [windows Media Format], wmformat.drm_play_opl, wmsdkidl/DRM_PLAY_OPL
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
 - DRM_PLAY_OPL
product: Windows
targetos: Windows
req.typenames: DRM_PLAY_OPL
req.redist: 
ms.custom: 19H1
---

# DRM_PLAY_OPL structure


## -description



The <b>DRM_PLAY_OPL</b> structure holds information about the output protection levels (OPL) specified in a license for play actions.




## -struct-fields




### -field minOPL


<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ns-wmsdkidl-__tagdrm_minimum_output_protection_levels">DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS</a> structure containing the minimum OPL required to play content in different formats.


### -field oplIdReserved

Reserved for future use.


### -field vopi


<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ns-wmsdkidl-__tagdrm_video_output_protection_ids">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a> structure containing the video output protection identifiers that apply to playback of the content.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ns-wmsdkidl-__tagdrm_copy_opl">DRM_COPY_OPL</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/structures">Structures</a>
 

 

