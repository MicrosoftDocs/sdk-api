---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_PROTECTION_FLAGS
title: MF_MEDIA_ENGINE_PROTECTION_FLAGS
author: windows-sdk-content
description: Contains flags that specify whether the Media Engine will play protected content, and whether the Media Engine will use the Protected Media Path (PMP).
old-location: mf\mf_media_engine_protection_flags.htm
tech.root: medfound
ms.assetid: 02326325-F122-4D6A-8CA7-3B201378BC15
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT, MF_MEDIA_ENGINE_PROTECTION_FLAGS, MF_MEDIA_ENGINE_PROTECTION_FLAGS enumeration [Media Foundation], MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT, MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP, mf.mf_media_engine_protection_flags, mfmediaengine/MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT, mfmediaengine/MF_MEDIA_ENGINE_PROTECTION_FLAGS, mfmediaengine/MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT, mfmediaengine/MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP
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
 - MF_MEDIA_ENGINE_PROTECTION_FLAGS
product: Windows
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_PROTECTION_FLAGS
req.redist: 
---

# MF_MEDIA_ENGINE_PROTECTION_FLAGS enumeration


## -description


Contains flags that specify whether the Media Engine will play protected content, and whether the Media Engine will use the <a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a> (PMP).


## -enum-fields




### -field MF_MEDIA_ENGINE_ENABLE_PROTECTED_CONTENT

Enable playback of protected content. The Media Engine will not play DRM-protected content unless this flag is set. If you set this flag, also set the <a href="https://msdn.microsoft.com/F6F17EC7-6553-4127-B691-C20C945DD4D8">MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER</a> attribute.


### -field MF_MEDIA_ENGINE_USE_PMP_FOR_ALL_CONTENT

Use the <a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a> (PMP) for all playback, including clear (non-protected) content.


### -field MF_MEDIA_ENGINE_USE_UNPROTECTED_PMP

Create the PMP inside an unprotected process. You can use this option to play clear content, but not to play protected content.


## -remarks



These flags are used with the <a href="https://msdn.microsoft.com/2A593499-BF40-440E-AF1D-3B0E7732489A">MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

