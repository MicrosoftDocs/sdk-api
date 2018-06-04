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

# DNS_FREE_TYPE enumeration


## -description


The <b>DNS_FREE_TYPE</b> enumeration specifies the type of data to free.


## -enum-fields




### -field DnsFreeFlat

The data freed is a flat structure.


### -field DnsFreeRecordList

The data freed is a Resource Record list, and includes subfields of the <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure. Resources freed include structures returned by the <a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> and <a href="https://msdn.microsoft.com/bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a">DnsRecordSetCopyEx</a> functions.


### -field DnsFreeParsedMessageFields

The data freed is a parsed message field.


## -see-also




<a href="https://msdn.microsoft.com/6ab53b19-7838-4e9f-9923-96a9267d2dbb">DNS Enumerations</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/83de7df8-7e89-42fe-b609-1dc173afc9df">DnsQueryConfig</a>



<a href="https://msdn.microsoft.com/bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a">DnsRecordSetCopyEx</a>
 

 

