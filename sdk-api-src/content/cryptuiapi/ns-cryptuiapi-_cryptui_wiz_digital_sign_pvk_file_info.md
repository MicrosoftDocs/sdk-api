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

# _CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/22d0bc45-0f66-4f5f-87d3-0849c4327eed">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a> structure to contain information about the PVK file used by the digital signature wizard.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field pwszPvkFileName

A pointer to a null-terminated Unicode string that contains the path and file name of the PVK file.


### -field pwszProvName

A pointer to a null-terminated Unicode string that contains the name of the provider.


### -field dwProvType

Contains the provider type identifier. For more information about the provider types, see <a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>.


## -see-also




<a href="https://msdn.microsoft.com/22d0bc45-0f66-4f5f-87d3-0849c4327eed">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a>



<a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>
 

 

