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

# FWPM_APPC_NETWORK_CAPABILITY_TYPE_ enumeration


## -description


The <b>FWPM_APPC_NETWORK_CAPABILITY_TYPE</b> enumeration specifies the type of app container network capability that is associated with the object or traffic in question.


## -enum-fields




### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT

Allows the app container to make network requests to servers on the Internet. It acts as a client.


### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER

Allows the app container to make requests and to receive requests to and from the Internet. It acts as a client and also as a server.


### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK

Allows the app container to make requests and to receive requests to and from private networks (such as a home network, work network, or the corporate domain network of the computer). It acts as a client and also as a server.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

