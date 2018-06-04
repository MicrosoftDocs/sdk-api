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

# DNS_PROXY_INFORMATION_TYPE enumeration


## -description



			The 
<b>DNS_PROXY_INFORMATION_TYPE</b> enumeration defines the proxy information type in the <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure.


## -enum-fields




### -field DNS_PROXY_INFORMATION_DIRECT

The type is bypass proxy information.


### -field DNS_PROXY_INFORMATION_DEFAULT_SETTINGS

The type is the user's default browser proxy settings.


### -field DNS_PROXY_INFORMATION_PROXY_NAME

The type is defined by the <b>proxyName</b> member of the <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure.


### -field DNS_PROXY_INFORMATION_DOES_NOT_EXIST

The type does not exist. DNS policy does not have proxy information for this name space. This type is used if no wildcard policy exists and there is no default proxy information.


## -see-also




<a href="https://msdn.microsoft.com/6ab53b19-7838-4e9f-9923-96a9267d2dbb">DNS Enumerations</a>
 

 

