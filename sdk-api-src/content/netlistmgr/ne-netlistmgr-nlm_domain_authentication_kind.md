---
UID: NE:netlistmgr.NLM_DOMAIN_AUTHENTICATION_KIND
title: NLM_DOMAIN_AUTHENTICATION_KIND
description: Defines constants that specify a domain authentication method.
tech.root: nla
ms.date: 04/07/2022
req.construct-type: enumeration
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NLM_DOMAIN_AUTHENTICATION_KIND
req.redist: 
ms.custom: 
f1_keywords:
 - NLM_DOMAIN_AUTHENTICATION_KIND
 - netlistmgr/NLM_DOMAIN_AUTHENTICATION_KIND
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netlistmgr.h
api_name:
 - NLM_DOMAIN_AUTHENTICATION_KIND
helpviewer_keywords:
 - NLM_DOMAIN_AUTHENTICATION_KIND
prerelease: false
---

## -description

Defines constants that specify a domain authentication method.

Only one of the listed constants is set for any instance of **DomainAuthenticationKind**. In some scenarios, the constant set will represent the most preferred protocol used to determine whether the domain was authenticated.

## -enum-fields

### -field NLM_DOMAIN_AUTHENTICATION_KIND_NONE

Specifies no domain authentication method; and/or that the network couldn't be domain-authenticated.

### -field NLM_DOMAIN_AUTHENTICATION_KIND_LDAP

Specifies the domain authentication method for an Active Directory network; and/or that the machine was successful in a Lightweight Directory Access Protocol (LDAP) authentication request against the configured Active Directory servers on the current network.

### -field NLM_DOMAIN_AUTHENTICATION_KIND_TLS

Specifies the Transport Layer Security (TLS) domain authentication method; and/or that the network connection was able to successfully complete a HTTPS connection with verified TLS authentication to an endpoint configured by the `AllowedTlsAuthenticationEndpoints` Mobile Device Management (MDM) policy.

## -remarks

## -see-also

* [INetwork2::IsDomainAuthenticatedBy method](nf-netlistmgr-inetwork2-isdomainauthenticatedby.md)
* [INetworkConnection2::IsDomainAuthenticatedBy method](nf-netlistmgr-inetworkconnection2-isdomainauthenticatedby.md)
