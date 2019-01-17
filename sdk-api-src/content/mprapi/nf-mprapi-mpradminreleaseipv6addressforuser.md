---
UID: NF:mprapi.MprAdminReleaseIpv6AddressForUser
title: MprAdminReleaseIpv6AddressForUser function
author: windows-sdk-content
description: The MprAdminReleaseIpv6AddressForUser function is called once for each user that needs to release an IPv6 address.
old-location: rras\mpradminreleaseipv6addressforuser.htm
tech.root: RRAS
ms.assetid: c06433b3-d1b0-42d0-993d-5c1cde4cbc0f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprAdminReleaseIpv6AddressForUser, MprAdminReleaseIpv6AddressForUser callback, MprAdminReleaseIpv6AddressForUser callback function [RAS], mprapi/MprAdminReleaseIpv6AddressForUser, rras.mpradminreleaseipv6addressforuser
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
 - MprAdminReleaseIpv6AddressForUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Pointer to an <a href="https://msdn.microsoft.com/2029db76-3fe1-4560-b753-910c48cbc578">IN6_ADDR</a> structure. This variable specifies the IPv6 address to be released.


## -returns



If function succeeds, the return value should be NO_ERROR.

If the function returns anything other than NO_ERROR, RAS will terminate the connection.




## -remarks



An administration DLL need not implement the 
<i>MprAdminReleaseIpv6AddressForUser</i> function. However, if the DLL implements 
<i>MprAdminReleaseIpv6AddressForUser</i>, it must also implement 
<a href="https://msdn.microsoft.com/ec4b4130-4864-470f-8647-1fcadd359c58">MprAdminGetIpv6AddressForUser</a>.




## -see-also




<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/ec4b4130-4864-470f-8647-1fcadd359c58">MprAdminGetIpv6AddressForUser</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

