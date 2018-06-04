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

# _DnsAddr structure


## -description


A <b>DNS_ADDR</b> structure stores an IPv4 or IPv6 address.


## -struct-fields




### -field MaxSa

A value that contains the socket IP address. It is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">sockaddr_in</a> structure if the address is IPv4 and a sockaddr_in6 structure if the address is IPv6.


### -field DnsAddrUserDword

Reserved. Must be 0.


## -see-also




<a href="https://msdn.microsoft.com/5FD7F28B-D1A6-4731-ACB9-A7BB23CC1FB4">DNS_ADDR_ARRAY</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>
 

 

