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

# lpmiptable structure


## -description


The 
<b>LPMIPTABLE</b> structure contains IP information, including the SNMP index, IP address, and subnet mask for each interface. The 
<b>LPMIPTABLE</b> structure is supplied as an argument for the <a href="https://msdn.microsoft.com/f02ecb97-3797-49a0-8bff-fcb16096cb25">Lpm_IpAddressTable</a> function.


## -struct-fields




### -field ulIfIndex

 


### -field MediaType

Media type of the interface.


### -field IfIpAddr

IP address for the interface.


### -field IfNetMask

IP subnet mask for the interface.


#### - UlIfIndex

SNMP index for the interface.


## -see-also




<a href="https://msdn.microsoft.com/f02ecb97-3797-49a0-8bff-fcb16096cb25">Lpm_IpAddressTable</a>
 

 

