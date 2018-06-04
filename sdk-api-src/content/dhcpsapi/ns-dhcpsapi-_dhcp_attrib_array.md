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

# _DHCP_ATTRIB_ARRAY structure


## -description


The <b>DHCP_ATTRIB_ARRAY</b> structure defines a set of DHCP server attributes.


## -struct-fields




### -field NumElements

Specifies the number of attributes listed in <b>DhcpAttribs</b>.


### -field DhcpAttribs

Pointer to a list of <a href="https://msdn.microsoft.com/26822137-8633-4e18-a69f-eeebf9e78f9a">DHCP_ATTRIB</a> structures that contain the DHCP server attributes.


### -field DhcpAttribs.size_is

 


### -field DhcpAttribs.size_is.NumElements

 



