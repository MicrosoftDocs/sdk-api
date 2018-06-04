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

# servent structure


## -description



			The 
<b>servent</b> structure is used to store or return the name and service number for a given service name.


## -struct-fields




### -field s_name

The official name of the service.


### -field s_aliases

A <b>NULL</b>-terminated array of alternate names.


### -field s_port

The port number at which the service can be contacted. Port numbers are returned in network byte order.


### -field s_proto

The name of the protocol to use when contacting the service.


## -see-also




<a href="https://msdn.microsoft.com/730fa372-f620-4d21-99b9-3e7b79932792">getservbyname</a>
 

 

