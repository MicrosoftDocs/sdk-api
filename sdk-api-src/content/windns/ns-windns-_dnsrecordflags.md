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

# _DnsRecordFlags structure


## -description



			The 
<b>DNS_RECORD_FLAGS</b> structure is used to set flags for use in the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure.


## -struct-fields




### -field Section

A <a href="https://msdn.microsoft.com/d51ef2c7-c2bb-4eed-a026-a559460352b6">DNS_SECTION</a> value that specifies the section of interest returned from the 
<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> function call.


### -field Delete

Reserved. Do not use.


### -field CharSet

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character set used in the associated function call.
					


### -field Unused

Reserved. Do not use.


### -field Reserved

Reserved. Do not use.


## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

