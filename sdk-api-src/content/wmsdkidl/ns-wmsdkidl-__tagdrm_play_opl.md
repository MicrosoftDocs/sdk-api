---
UID: NS:wmsdkidl.__tagDRM_PLAY_OPL
title: "__tagDRM_PLAY_OPL"
author: windows-sdk-content
description: The DRM_PLAY_OPL structure holds information about the output protection levels (OPL) specified in a license for play actions.
old-location: wmformat\drm_play_opl.htm
old-project: wmformat
ms.assetid: 5d14bd02-0fb5-4982-b3dc-7f8277cb852f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DRM_PLAY_OPL, DRM_PLAY_OPL structure [windows Media Format], __tagDRM_PLAY_OPL, structure [windows Media Format], wmformat.drm_play_opl, wmsdkidl/DRM_PLAY_OPL
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
tech.root: 
req.typenames: DRM_PLAY_OPL
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

