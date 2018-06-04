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

# NET_ADDRESS_FORMAT_ enumeration


## -description


The <b>NET_ADDRESS_FORMAT</b> enumeration specifies the format of a network address returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function.


## -enum-fields




### -field NET_ADDRESS_FORMAT_UNSPECIFIED

The format of the network address is unspecified.


### -field NET_ADDRESS_DNS_NAME

The format of the network address is a DNS name.


### -field NET_ADDRESS_IPV4

The format of the network address is a string in Internet standard dotted-decimal notation for IPv4.



### -field NET_ADDRESS_IPV6

The format of the network address is a string in Internet standard hexadecimal encoding for IPv6.



## -remarks



The <b>NET_ADDRESS_FORMAT</b> enumeration is defined on Windows Vista and later. 

The <b>NET_ADDRESS_FORMAT</b> enumeration is used in the <a href="https://msdn.microsoft.com/1a59cc13-a3fc-4489-aafd-444a96d9a339">NET_ADDRESS_INFO</a> structure returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/1a59cc13-a3fc-4489-aafd-444a96d9a339">NET_ADDRESS_INFO</a>



<a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a>
 

 

