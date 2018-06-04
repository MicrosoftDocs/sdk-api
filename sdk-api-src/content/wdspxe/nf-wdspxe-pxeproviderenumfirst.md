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

# PxeProviderEnumFirst function


## -description


Starts an enumeration of registered providers.


## -parameters




### -param phEnum [out]

Address of a <b>HANDLE</b> that on successful return can be used with the 
      <a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a> function to enumerate 
      providers. When the enumeration handle is no longer needed, use the 
      <a href="https://msdn.microsoft.com/6b71c2cf-a156-4ccb-be7c-2955b4db26a2">PxeProviderEnumClose</a> function to close the 
      enumeration.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/6b71c2cf-a156-4ccb-be7c-2955b4db26a2">PxeProviderEnumClose</a>



<a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

