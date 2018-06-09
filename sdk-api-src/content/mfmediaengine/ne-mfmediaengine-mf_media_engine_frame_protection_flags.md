---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
title: MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
author: windows-sdk-content
description: Specifies the content protection requirements for a video frame.
old-location: mf\mf_media_engine_frame_protection_flags.htm
old-project: medfound
ms.assetid: 6864ED4B-BB75-4176-992B-ABC95B81001A
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS, MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS enumeration [Media Foundation], MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED, MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION, MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION, mf.mf_media_engine_frame_protection_flags, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION, mfmediaengine/MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS enumeration


## -description


Specifies the content protection requirements for a video frame.


## -enum-fields




### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED

The video frame should be protected.


### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION

Direct3D surface protection must be applied to any surface that contains the frame.


### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION

Direct3D anti-screen-scrape protection must be applied to any surface that contains the frame.


## -see-also




<a href="https://msdn.microsoft.com/4D67813D-F222-4EB1-B059-6DB5EC642DA2">IMFMediaEngineProtectedContent::GetRequiredProtections</a>



<a href="https://msdn.microsoft.com/3A5C6908-65F4-4E7A-AD71-BBD1C2A4ACE3">IMFMediaEngineProtectedContent::TransferVideoFrame</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

