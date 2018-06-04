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

# MI_HostedProvider_Close function


## -description


Close a hosted provider handle that was returned from <a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a>.


## -parameters




### -param hostedProvider [in, out]

A pointer to a provider handle returned from the <a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a> function.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



When this function returns, no new calls will enter the provider.




## -see-also




<a href="https://msdn.microsoft.com/4f39ffca-4ae3-4ce5-9460-c7ac27c06a50">MI_Application_NewHostedProvider</a>



<a href="https://msdn.microsoft.com/26afde05-6ef6-4044-b8a1-fad2a3bb4385">MI_HostedProvider_GetApplication</a>
 

 

