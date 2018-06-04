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

# DnsGetProxyInformation function


## -description


The 
<b>DnsGetProxyInformation</b> function returns the proxy information for a DNS server's name resolution policy table.


## -parameters




### -param hostName [in]

A pointer to a string that represents the name of the DNS server whose proxy information is returned.


### -param proxyInformation [in, out]

A pointer to a <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure that contains the proxy information for <i>hostName</i>.


### -param defaultProxyInformation [in, out, optional]

A pointer to a <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure that contains the default proxy information for <i>hostName</i>. This proxy information is for the wildcard DNS policy.


### -param completionRoutine [in, optional]

Reserved. Do not use.


### -param completionContext [in, optional]

Reserved. Do not use.


## -returns



The 
<b>DnsGetProxyInformation</b> function returns the appropriate DNS-specific error code as defined in Winerror.h. The following are possible return values:




## -see-also




<a href="https://msdn.microsoft.com/9b3c1c20-5516-41de-b00f-b95736ff53f1">DNS Functions</a>
 

 

