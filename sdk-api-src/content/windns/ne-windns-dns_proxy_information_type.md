---
UID: NE:windns.DNS_PROXY_INFORMATION_TYPE
title: DNS_PROXY_INFORMATION_TYPE
author: windows-sdk-content
description: The DNS_PROXY_INFORMATION_TYPE enumeration defines the proxy information type in the DNS_PROXY_INFORMATION structure.
old-location: dns\dns_proxy_information_type.htm
tech.root: dns
ms.assetid: 983d38f3-3ee7-4df6-a9ff-f908f250020f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DNS_PROXY_INFORMATION_DEFAULT_SETTINGS, DNS_PROXY_INFORMATION_DIRECT, DNS_PROXY_INFORMATION_DOES_NOT_EXIST, DNS_PROXY_INFORMATION_PROXY_NAME, DNS_PROXY_INFORMATION_TYPE, DNS_PROXY_INFORMATION_TYPE enumeration [DNS], dns.dns_proxy_information_type, windns/DNS_PROXY_INFORMATION_DEFAULT_SETTINGS, windns/DNS_PROXY_INFORMATION_DIRECT, windns/DNS_PROXY_INFORMATION_DOES_NOT_EXIST, windns/DNS_PROXY_INFORMATION_PROXY_NAME, windns/DNS_PROXY_INFORMATION_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_PROXY_INFORMATION_TYPE
product: Windows
targetos: Windows
req.typenames: DNS_PROXY_INFORMATION_TYPE
req.redist: 
---

# DNS_PROXY_INFORMATION_TYPE enumeration


## -description


The 
<b>DNS_PROXY_INFORMATION_TYPE</b> enumeration defines the proxy information type in the <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure.


## -enum-fields




### -field DNS_PROXY_INFORMATION_DIRECT

The type is bypass proxy information.


### -field DNS_PROXY_INFORMATION_DEFAULT_SETTINGS

The type is the user's default browser proxy settings.


### -field DNS_PROXY_INFORMATION_PROXY_NAME

The type is defined by the <b>proxyName</b> member of the <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure.


### -field DNS_PROXY_INFORMATION_DOES_NOT_EXIST

The type does not exist. DNS policy does not have proxy information for this name space. This type is used if no wildcard policy exists and there is no default proxy information.


## -see-also




<a href="https://msdn.microsoft.com/6ab53b19-7838-4e9f-9923-96a9267d2dbb">DNS Enumerations</a>
 

 

