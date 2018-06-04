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

# __MIDL_IWTSSBPlugin_0006 structure


## -description


Contains information about a computer that is accepting remote connections.


## -struct-fields




### -field wczMachineFQDN

The fully qualified domain name (FQDN) of the computer.  The name cannot exceed 256 characters.


### -field wczMachineNetBiosName

The NetBIOS name of the computer. The name cannot exceed 16 characters.


### -field dwNumOfIPAddr

The number of IP addresses that are configured on the computer.


### -field IPaddr

An array of <a href="https://msdn.microsoft.com/92fe662a-ad31-4ed3-9393-c7d86f97e702">WTSSBX_IP_ADDRESS</a> structures that indicate the IP addresses on this computer that are visible to Remote Desktop Connection (RDC) clients. This array cannot exceed 12 elements.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

