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

# _WNV_IP_ADDRESS structure


## -description


Defines an IP address object.


## -struct-fields




### -field IP

An IP version 4 (IPv4) or IP version 6 (IPv6) address object.


### -field IP.v4

<b>Type: <b>IN_ADDR</b>
</b>
An IPv4 address.


### -field IP.v6

<b>Type: <b>IN6_ADDR</b>
</b>
An IPv6 address.


### -field IP.Addr

<b>Type: <b>UCHAR[sizeof(IN6_ADDR)]</b>
</b>
An array of bytes that contains the IP address.


## -remarks



The <b>ADDRESS_FAMILY</b> value is always specified separately in the structures that contain this IP address object.



