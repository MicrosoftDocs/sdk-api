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

# CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure


## -description


Represents IP information for a NetName resource that has Multichannel enabled.


## -struct-fields




### -field szName

An array of wide characters that specifies the name of the resource.


### -field NumEntries

The number of channels that are specified by the <i>IpInfo</i> parameter.


### -field IpInfo

An array of <a href="https://msdn.microsoft.com/9631BDB9-6B7C-4BFF-9654-20C77F851A22">CLUS_NETNAME_IP_INFO_ENTRY</a> structures that specify the IP info for each channel.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

