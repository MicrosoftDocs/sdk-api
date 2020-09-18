---
UID: NF:mprapi.MprAdminReleaseIpv6AddressForUser
title: MprAdminReleaseIpv6AddressForUser function (mprapi.h)
description: The MprAdminReleaseIpv6AddressForUser function is called once for each user that needs to release an IPv6 address.
helpviewer_keywords: ["MprAdminReleaseIpv6AddressForUser","MprAdminReleaseIpv6AddressForUser callback","MprAdminReleaseIpv6AddressForUser callback function [RAS]","mprapi/MprAdminReleaseIpv6AddressForUser","rras.mpradminreleaseipv6addressforuser"]
old-location: rras\mpradminreleaseipv6addressforuser.htm
tech.root: RRAS
ms.assetid: c06433b3-d1b0-42d0-993d-5c1cde4cbc0f
ms.date: 12/05/2018
ms.keywords: MprAdminReleaseIpv6AddressForUser, MprAdminReleaseIpv6AddressForUser callback, MprAdminReleaseIpv6AddressForUser callback function [RAS], mprapi/MprAdminReleaseIpv6AddressForUser, rras.mpradminreleaseipv6addressforuser
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
 - MprAdminReleaseIpv6AddressForUser
 - mprapi/MprAdminReleaseIpv6AddressForUser
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
 - MprAdminReleaseIpv6AddressForUser
---

# MprAdminReleaseIpv6AddressForUser function


## -description

The 
<i>MprAdminReleaseIpv6AddressForUser</i> function is called once for each user that needs to release an IPv6 address.

## -parameters

### -param lpszUserName [in]

Pointer to a Unicode string that specifies the name of the user that disconnected.

### -param lpszPortName [in]

Pointer to a Unicode string that specifies the name of the port on which the user disconnected.

### -param lpdwIpv6Address [in]

Pointer to an <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure. This variable specifies the IPv6 address to be released.

## -returns

If function succeeds, the return value should be NO_ERROR.

If the function returns anything other than NO_ERROR, RAS will terminate the connection.

## -remarks

An administration DLL need not implement the 
<i>MprAdminReleaseIpv6AddressForUser</i> function. However, if the DLL implements 
<i>MprAdminReleaseIpv6AddressForUser</i>, it must also implement 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipv6addressforuser">MprAdminGetIpv6AddressForUser</a>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipv6addressforuser">MprAdminGetIpv6AddressForUser</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>