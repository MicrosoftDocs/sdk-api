---
UID: NF:windns.DnsAcquireContextHandle_A
title: DnsAcquireContextHandle_A function (windns.h)
description: The DnsAcquireContextHandle function type acquires a context handle to a set of credentials.helpviewer_keywords: ["DnsAcquireContextHandle","DnsAcquireContextHandle function [DNS]","DnsAcquireContextHandle_A","DnsAcquireContextHandle_W","_dns_dnsacquirecontexthandle","dns.dnsacquirecontexthandle","windns/DnsAcquireContextHandle","windns/DnsAcquireContextHandle_A","windns/DnsAcquireContextHandle_W"]
old-location: dns\dnsacquirecontexthandle.htm
tech.root: DNS
ms.assetid: 9a820165-2f78-44f4-b49f-dc7a2b6fb4e5
ms.date: 12/05/2018
ms.keywords: DnsAcquireContextHandle, DnsAcquireContextHandle function [DNS], DnsAcquireContextHandle_A, DnsAcquireContextHandle_W, _dns_dnsacquirecontexthandle, dns.dnsacquirecontexthandle, windns/DnsAcquireContextHandle, windns/DnsAcquireContextHandle_A, windns/DnsAcquireContextHandle_W
f1_keywords:
- windns/DnsAcquireContextHandle
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DnsAcquireContextHandle_A function


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

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY_W</a> structure or a <b>SEC_WINNT_AUTH_IDENTITY_A</b> structure that contains the name, domain, and password of the account to be used in a secure dynamic update. If <i>CredentialFlags</i> is set to <b>TRUE</b>, <i>Credentials</i> points to a <b>SEC_WINNT_AUTH_IDENTITY_W</b> structure; otherwise, <i>Credentials</i> points to a <b>SEC_WINNT_AUTH_IDENTITY_A</b> structure. If not specified, the credentials of the calling service are used. This parameter is optional.


### -param pContext [out]

A pointer to a handle pointing to the returned credentials.


## -returns



Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a>
 

 

