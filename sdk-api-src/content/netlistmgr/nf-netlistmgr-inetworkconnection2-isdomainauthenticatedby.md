---
UID: NF:netlistmgr.INetworkConnection2.IsDomainAuthenticatedBy
title: INetworkConnection2::IsDomainAuthenticatedBy
description: Queries whether the specified domain authentication method succeeded for this network connection.
tech.root: nla
ms.date: 04/07/2022
req.construct-type: function
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
req.typenames: 
req.redist: 
f1_keywords:
 - INetworkConnection2::IsDomainAuthenticatedBy
 - netlistmgr/INetworkConnection2::IsDomainAuthenticatedBy
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - netlistmgr.h
api_name:
 - INetworkConnection2::IsDomainAuthenticatedBy
helpviewer_keywords:
 - IsDomainAuthenticatedBy
prerelease: false
---

## -description

Queries whether the specified domain authentication method succeeded for this network connection.

## -parameters

### -param domainAuthenticationKind

Type: \[in\] **[NLM_DOMAIN_AUTHENTICATION_KIND](ne-netlistmgr-nlm_domain_authentication_kind.md)**

The specific domain authentication method to query about.

### -param pValue

Type: \[out, retval\] **[BOOL](/windows/win32/winprog/windows-data-types)\***

The function dereferences *pValue*, and assigns `TRUE` if this network connection has the same domain authentication kind as that specified in the *domainAuthenticationKind* parameter; or `FALSE` if this network connection has a different domain authentication kind from that specified in *domainAuthenticationKind*.

## -returns

Returns **S_OK** if successful.

## -remarks

See **Remarks** for [INetwork2::IsDomainAuthenticatedBy method](nf-netlistmgr-inetwork2-isdomainauthenticatedby.md).

## Example

See **Example** for [INetwork2::IsDomainAuthenticatedBy method](nf-netlistmgr-inetwork2-isdomainauthenticatedby.md).

## -see-also

* [INetwork2::IsDomainAuthenticatedBy method](nf-netlistmgr-inetwork2-isdomainauthenticatedby.md)
