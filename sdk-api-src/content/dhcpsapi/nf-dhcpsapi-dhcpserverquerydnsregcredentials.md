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

# DhcpServerQueryDnsRegCredentials function


## -description


The <b>DhcpServerQueryDnsRegCredentials</b> function retrieves the current Domain Name System (DNS) credentials used by the DHCP server for client dynamic DNS registration.


## -parameters




### -param ServerIpAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_SRV_HANDLE</a> that specifies the RPC binding to the DHCP server that will be queried.


### -param UnameSize [in]

Unsigned 32-bit integer that indicates the size, in bytes, to allocate for the data returned in the <i>Uname</i> buffer.


### -param Uname [out]

Pointer to a null-terminated Unicode string that contains the user name for the DNS server credentials. The size of this value cannot be larger than the size specified in <i>UnameSize</i>.


### -param DomainSize [in]

Unsigned 32-bit integer that indicates the size, in bytes, to allocate for the data returned in the <i>Domain</i> buffer.


### -param Domain [out]

Pointer to a null-terminated Unicode string that contains the domain name for the DNS server credentials. The size of this value cannot be larger than the size specified in <i>DomainSize</i>.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



DNS credentials can be set on the DHCP server by calling the <a href="https://msdn.microsoft.com/7fed2635-43a6-417a-996f-fff8d0692924">DhcpServerSetDnsRegCredentialsV5</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7fed2635-43a6-417a-996f-fff8d0692924">DhcpServerSetDnsRegCredentialsV5</a>
 

 

