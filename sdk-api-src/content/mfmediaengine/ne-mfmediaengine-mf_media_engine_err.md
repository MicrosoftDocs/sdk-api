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

# MF_MEDIA_ENGINE_ERR enumeration


## -description


Defines error status codes for the Media Engine.


## -enum-fields




### -field MF_MEDIA_ENGINE_ERR_NOERROR

No error.


### -field MF_MEDIA_ENGINE_ERR_ABORTED

The process of fetching the media resource was stopped at the user's request. 


### -field MF_MEDIA_ENGINE_ERR_NETWORK

A network error occurred while fetching the media resource. 


### -field MF_MEDIA_ENGINE_ERR_DECODE

An error occurred while decoding the media resource. 


### -field MF_MEDIA_ENGINE_ERR_SRC_NOT_SUPPORTED

The media resource is not supported. 


### -field MF_MEDIA_ENGINE_ERR_ENCRYPTED

An error occurred while encrypting the media resource.

Supported in Windows 8.1 and later.


## -remarks



The values greater than zero correspond to error codes defined for the <b>MediaError</b> object  in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/6E4C4559-F59C-488C-A790-D95831BC9D29">IMFMediaError::GetErrorCode</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

