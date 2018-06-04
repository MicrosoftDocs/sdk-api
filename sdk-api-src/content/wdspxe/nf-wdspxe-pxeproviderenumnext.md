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

# PxeProviderEnumNext function


## -description


Enumerates registered providers.


## -parameters




### -param hEnum [in]

<b>HANDLE</b> returned by the 
      <a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a> function.


### -param ppProvider [out]

Address of a <a href="https://msdn.microsoft.com/a07afefd-7a97-42bb-8d70-2bc7c51ddef3">PXE_PROVIDER</a> structure with the 
      <b>uSizeOfStruct</b> member filled in with the size of the structure. On return this 
      structure is filled in with provider information. This structure can be freed with the 
      <a href="https://msdn.microsoft.com/dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7">PxeProviderFreeInfo</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/a07afefd-7a97-42bb-8d70-2bc7c51ddef3">PXE_PROVIDER</a>



<a href="https://msdn.microsoft.com/6b71c2cf-a156-4ccb-be7c-2955b4db26a2">PxeProviderEnumClose</a>



<a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a>



<a href="https://msdn.microsoft.com/dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7">PxeProviderFreeInfo</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

