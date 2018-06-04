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
 

 

