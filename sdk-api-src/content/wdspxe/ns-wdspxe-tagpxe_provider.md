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

# tagPXE_PROVIDER structure


## -description


Describes a provider.


## -struct-fields




### -field uSizeOfStruct

Size of the <b>PXE_PROVIDER</b> structure.


### -field pwszName

Address of a null-terminated string that specifies the display name of the provider. This name is displayed 
      to the user and must be unique among registered providers.


### -field pwszFilePath

Address of a null-terminated string that specifies the full path to the provider DLL.


### -field bIsCritical

Indicates whether the provider is critical. If a critical provider fails, the WDS server will also 
      fail.


### -field uIndex

Index of a provider in the list of registered providers.


## -see-also




<a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a>



<a href="https://msdn.microsoft.com/dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7">PxeProviderFreeInfo</a>



<a href="https://msdn.microsoft.com/2e52a6ae-cecb-45de-b777-108836ed5264">Windows Deployment Services Structures</a>
 

 

