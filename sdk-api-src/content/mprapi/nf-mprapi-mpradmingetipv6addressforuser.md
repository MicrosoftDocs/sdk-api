---
UID: NF:mprapi.MprAdminGetIpv6AddressForUser
title: MprAdminGetIpv6AddressForUser function (mprapi.h)
author: windows-sdk-content
description: RAS calls the MprAdminGetIpv6AddressForUser function once for each user that requires an IPv6 address.
old-location: rras\mpradmingetipv6addressforuser.htm
tech.root: RRAS
ms.assetid: ec4b4130-4864-470f-8647-1fcadd359c58
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprAdminGetIpv6AddressForUser, MprAdminGetIpv6AddressForUser callback, MprAdminGetIpv6AddressForUser callback function [RAS], mprapi/MprAdminGetIpv6AddressForUser, rras.mpradmingetipv6addressforuser
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminGetIpv6AddressForUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Pointer to an <a href="https://msdn.microsoft.com/2029db76-3fe1-4560-b753-910c48cbc578">in6_addr</a> structure that contains zero or the IPv6 address RAS allocated for the user. 


Currently, only 64 bit identifiers are supported.

On output, if RAS specified zero, the DLL allocates an IPv6 address for the user. In this case, if the DLL does not allocate an IPv6 address, the user is not able to connect. If RAS specified an IPv6 address, the DLL either accepts the address or substitutes a different one.


### -param bNotifyRelease [out]

Pointer to a <b>BOOL</b> variable. If the DLL sets this variable to <b>TRUE</b>, RAS  calls 
<a href="https://msdn.microsoft.com/c06433b3-d1b0-42d0-993d-5c1cde4cbc0f">MprAdminReleaseIpv6AddressForUser</a> when the user disconnects. Otherwise, RAS does not notify the DLL when this IP address is released.


## -returns



If function succeeds, the return value should be NO_ERROR.

If the function returns anything other than NO_ERROR, RAS will terminate the connection.




## -remarks



An administration DLL need not implement the 
<i>MprAdminGetIpv6AddressForUser</i> function. However, if the DLL implements 
<i>MprAdminGetIpv6AddressForUser</i>, it must also implement 
<a href="https://msdn.microsoft.com/c06433b3-d1b0-42d0-993d-5c1cde4cbc0f">MprAdminReleaseIpv6AddressForUser</a>.




## -see-also




<a href="https://msdn.microsoft.com/c06433b3-d1b0-42d0-993d-5c1cde4cbc0f">MprAdminReleaseIpv6AddressForUser</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

