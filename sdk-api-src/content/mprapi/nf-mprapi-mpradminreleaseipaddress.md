---
UID: NF:mprapi.MprAdminReleaseIpAddress
title: MprAdminReleaseIpAddress function (mprapi.h)
description: The MprAdminReleaseIpAddress function is called when a user disconnects and the user's IP address is about to be released.
helpviewer_keywords: ["MprAdminReleaseIpAddress","MprAdminReleaseIpAddress callback","MprAdminReleaseIpAddress callback function [RAS]","_mpr_mpradminreleaseipaddress","mprapi/MprAdminReleaseIpAddress","rras.mpradminreleaseipaddress"]
old-location: rras\mpradminreleaseipaddress.htm
tech.root: RRAS
ms.assetid: 7a1570a9-b43f-4603-a5ed-6d078a5bbb7c
ms.date: 12/05/2018
ms.keywords: MprAdminReleaseIpAddress, MprAdminReleaseIpAddress callback, MprAdminReleaseIpAddress callback function [RAS], _mpr_mpradminreleaseipaddress, mprapi/MprAdminReleaseIpAddress, rras.mpradminreleaseipaddress
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - MprAdminReleaseIpAddress
 - mprapi/MprAdminReleaseIpAddress
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
 - MprAdminReleaseIpAddress
---

# MprAdminReleaseIpAddress function


## -description

The 
<b>MprAdminReleaseIpAddress</b> function is called when a user disconnects and the user's IP address is about to be released.

## -parameters

### -param lpszUserName [in]

Pointer to a Unicode string that specifies the name of the user that requires an IP address.

### -param lpszPortName [in]

Pointer to a Unicode string that specifies the name of the port on which the user is attempting to connect.

### -param lpdwIpAddress [in]

Pointer to a <b>DWORD</b> variable. This variable specifies the IP address to be released.

## -remarks

An administration DLL need not implement the 
<b>MprAdminReleaseIpAddress</b> function. However, if the DLL implements 
<b>MprAdminReleaseIpAddress</b>, it must also implement 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipaddressforuser">MprAdminGetIpAddressForUser</a>.

RAS supports multiple Administration DLLs. However, RAS calls 
<b>MprAdminReleaseIpAddress</b> only in the first DLL that implements and export it. RAS ignores implementations of these functions in the other DLLs. RAS checks the DLLs for these functions in the order in which they are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.

<b>Windows 2000 Server or earlier:  </b>If RAS does not accept the new link, RAS does not call the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminlinkhangupnotification">MprAdminLinkHangupNotification</a> function.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminReleaseIpAddress</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipaddressforuser">MprAdminGetIpAddressForUser</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>