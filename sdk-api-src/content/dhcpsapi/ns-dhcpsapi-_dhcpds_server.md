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

# _DHCPDS_SERVER structure


## -description


The <b>DHCPDS_SERVER</b> structure defines information on a DHCP server in the context of directory services.


## -struct-fields




### -field Version

Reserved. This value should be set to 0.


### -field ServerName

Unicode string that contains the unique name of the DHCP server.


### -field ServerAddress

Specifies the IP address of the DHCP server as an unsigned 32-bit integer.


### -field Flags

Specifies a set of bit flags that describe active directory settings for the DHCP server.


### -field State

Reserved. This value should be set to 0.


### -field DsLocation

Unicode string that contains the active directory path to the DHCP server.


### -field DsLocType

Reserved. This value should be set to 0.

