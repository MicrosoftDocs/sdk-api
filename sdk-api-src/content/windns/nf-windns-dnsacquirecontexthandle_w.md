---
UID: NF:windns.DnsAcquireContextHandle_W
title: DnsAcquireContextHandle_W function
author: windows-sdk-content
description: The DnsAcquireContextHandle function type acquires a context handle to a set of credentials.
old-location: dns\dnsacquirecontexthandle.htm
tech.root: DNS
ms.assetid: 9a820165-2f78-44f4-b49f-dc7a2b6fb4e5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DnsAcquireContextHandle, DnsAcquireContextHandle function [DNS], DnsAcquireContextHandle_A, DnsAcquireContextHandle_W, _dns_dnsacquirecontexthandle, dns.dnsacquirecontexthandle, windns/DnsAcquireContextHandle, windns/DnsAcquireContextHandle_A, windns/DnsAcquireContextHandle_W
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DnsAcquireContextHandle_W (Unicode) and DnsAcquireContextHandle_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsAcquireContextHandle
 - DnsAcquireContextHandle_A
 - DnsAcquireContextHandle_W
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsAcquireContextHandle_W function


## -description


The 
<b>DnsAcquireContextHandle</b> function type acquires a context handle to a set of credentials. Like many DNS functions, the 
<b>DnsAcquireContextHandle</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li>
<b>DnsAcquireContextHandle_A</b> (_A for ANSI encoding)

</li>
<li>
<b>DnsAcquireContextHandle_W</b> (_W for Unicode encoding)

</li>
</ul>

## -parameters




### -param CredentialFlags [in]

A flag that indicates the character encoding. Set to <b>TRUE</b> for Unicode, <b>FALSE</b> for ANSI.


### -param Credentials [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/829dee24-aeeb-4191-b5fc-85970725f064">SEC_WINNT_AUTH_IDENTITY_W</a> structure or a <b>SEC_WINNT_AUTH_IDENTITY_A</b> structure that contains the name, domain, and password of the account to be used in a secure dynamic update. If <i>CredentialFlags</i> is set to <b>TRUE</b>, <i>Credentials</i> points to a <b>SEC_WINNT_AUTH_IDENTITY_W</b> structure; otherwise, <i>Credentials</i> points to a <b>SEC_WINNT_AUTH_IDENTITY_A</b> structure. If not specified, the credentials of the calling service are used. This parameter is optional.


### -param pContext [out]

A pointer to a handle pointing to the returned credentials.


## -returns



Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/829dee24-aeeb-4191-b5fc-85970725f064">SEC_WINNT_AUTH_IDENTITY</a>
 

 

