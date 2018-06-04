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

# DhcpServerSetDnsRegCredentialsV5 function


## -description


The <b>DhcpServerSetDnsRegCredentialsV5</b> function sets the credentials used by the DHCP server to create Domain Name System (DNS) registrations for the DHCP client lease record.


## -parameters




### -param ServerIpAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_SRV_HANDLE</a> that specifies the RPC binding to the DHCP server  on which the DNS credentials will be set.


### -param Uname [in]

Pointer to a null-terminated Unicode string that specifies the user name for the DNS credentials.


### -param Domain [in]

Pointer to a null-terminated Unicode string that specifies the domain name for the DNS credentials.


### -param Passwd

TBD




#### - Password [in]

Pointer to a null-terminated   Unicode string that specifies the password for the DNS credentials. The password can be unencrypted.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/773cbfef-1dc5-4d44-9997-591acbfb3783">DhcpServerQueryDnsRegCredentials</a>
 

 

