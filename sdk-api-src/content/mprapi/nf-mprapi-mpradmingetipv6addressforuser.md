---
UID: NF:mprapi.MprAdminGetIpv6AddressForUser
title: MprAdminGetIpv6AddressForUser function (mprapi.h)
description: RAS calls the MprAdminGetIpv6AddressForUser function once for each user that requires an IPv6 address.
helpviewer_keywords: ["MprAdminGetIpv6AddressForUser","MprAdminGetIpv6AddressForUser callback","MprAdminGetIpv6AddressForUser callback function [RAS]","mprapi/MprAdminGetIpv6AddressForUser","rras.mpradmingetipv6addressforuser"]
old-location: rras\mpradmingetipv6addressforuser.htm
tech.root: RRAS
ms.assetid: ec4b4130-4864-470f-8647-1fcadd359c58
ms.date: 12/05/2018
ms.keywords: MprAdminGetIpv6AddressForUser, MprAdminGetIpv6AddressForUser callback, MprAdminGetIpv6AddressForUser callback function [RAS], mprapi/MprAdminGetIpv6AddressForUser, rras.mpradmingetipv6addressforuser
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminGetIpv6AddressForUser
 - mprapi/MprAdminGetIpv6AddressForUser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminGetIpv6AddressForUser
---

# MprAdminGetIpv6AddressForUser function


## -description

RAS calls 
the <i>MprAdminGetIpv6AddressForUser</i>  function once for each user that requires an IPv6 address. RAS calls the function with the IPv6 address that RAS selects for the user. The third-party DLL that implements this function can change this address to one of its own choosing.

## -parameters

### -param lpwszUserName [in]

Pointer to a Unicode string that specifies the name of the user that requires an IP address.

### -param lpwszPortName [in]

Pointer to a Unicode string that specifies the name of the port on which the user is attempting to connect.

### -param lpdwIpv6Address [in, out]

Pointer to an <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">in6_addr</a> structure that contains zero or the IPv6 address RAS allocated for the user. 


Currently, only 64 bit identifiers are supported.

On output, if RAS specified zero, the DLL allocates an IPv6 address for the user. In this case, if the DLL does not allocate an IPv6 address, the user is not able to connect. If RAS specified an IPv6 address, the DLL either accepts the address or substitutes a different one.

### -param bNotifyRelease [out]

Pointer to a <b>BOOL</b> variable. If the DLL sets this variable to <b>TRUE</b>, RAS  calls 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipv6addressforuser">MprAdminReleaseIpv6AddressForUser</a> when the user disconnects. Otherwise, RAS does not notify the DLL when this IP address is released.

## -returns

If function succeeds, the return value should be NO_ERROR.

If the function returns anything other than NO_ERROR, RAS will terminate the connection.

## -remarks

An administration DLL need not implement the 
<i>MprAdminGetIpv6AddressForUser</i> function. However, if the DLL implements 
<i>MprAdminGetIpv6AddressForUser</i>, it must also implement 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipv6addressforuser">MprAdminReleaseIpv6AddressForUser</a>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipv6addressforuser">MprAdminReleaseIpv6AddressForUser</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>