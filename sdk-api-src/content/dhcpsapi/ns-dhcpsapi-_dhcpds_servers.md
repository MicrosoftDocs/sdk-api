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

# _DHCPDS_SERVERS structure


## -description


The <b>DHCPDS_SERVERS</b> structure defines a list of DHCP servers in the context of directory services.


## -struct-fields




### -field Flags

Reserved. This value should be 0.


### -field NumElements

Specifies the number of elements in <b>Servers</b>.


### -field Servers

Pointer to an array of <a href="https://msdn.microsoft.com/12f3fbd3-9b81-4a11-914c-83658c2bce89">DHCPDS_SERVER</a> structures that contain information on individual DHCP servers.

