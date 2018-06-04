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

# __MIDL___MIDL_itf_mfidl_0000_0031_0001 enumeration


## -description



Indicates whether the URL is from a trusted source.




## -enum-fields




### -field MF_LICENSE_URL_UNTRUSTED

The validity of the URL cannot be guaranteed because it is not signed. The application should warn the user.


### -field MF_LICENSE_URL_TRUSTED

The URL is the original one provided with the content.


### -field MF_LICENSE_URL_TAMPERED

The URL was originally signed and has been tampered with. The file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.


## -see-also




<a href="https://msdn.microsoft.com/1a44216d-36e5-4b5c-9585-5297d5e429f9">IMFContentEnabler::GetEnableURL</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

