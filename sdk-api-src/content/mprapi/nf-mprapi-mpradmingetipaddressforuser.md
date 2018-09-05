---
UID: NF:mprapi.MprAdminGetIpAddressForUser
title: MprAdminGetIpAddressForUser function
author: windows-sdk-content
description: RAS calls the MprAdminGetIpAddressForUser function once for each user that requires an IP address.
old-location: rras\mpradmingetipaddressforuser.htm
old-project: RRAS
ms.assetid: 79deeb39-1916-4bb0-b701-8f0a05dc55af
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MprAdminGetIpAddressForUser, MprAdminGetIpAddressForUser callback, MprAdminGetIpAddressForUser callback function [RAS], _mpr_mpradmingetipaddressforuser, mprapi/MprAdminGetIpAddressForUser, rras.mpradmingetipaddressforuser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminGetIpAddressForUser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminGetIpAddressForUser function


## -description


RAS calls 
the <b>MprAdminGetIpAddressForUser</b>  function once for each user that requires an IP address. RAS calls the function with the IP address that RAS selects for the user. The third-party DLL that implements this function can change this address to one of its own choosing.


## -parameters




### -param lpwszUserName [in]

Pointer to a Unicode string that specifies the name of the user that requires an IP address.


### -param lpwszPortName [in]

Pointer to a Unicode string that specifies the name of the port on which the user is attempting to connect.


### -param lpdwIpAddress [in, out]

On input, pointer to a <b>DWORD</b> variable that contains zero or the IP address RAS allocated for the user. 




On output, if RAS specified zero, the DLL allocates an IP address for the user. In this case, if the DLL does not allocate an IP address, the user is not able to connect. If RAS specified an IP address, the DLL either accepts the address or substitutes a different one.


### -param bNotifyRelease [out]

Pointer to a <b>BOOL</b> variable. If the DLL sets this variable to <b>TRUE</b>, RAS  calls 
<a href="https://msdn.microsoft.com/7a1570a9-b43f-4603-a5ed-6d078a5bbb7c">MprAdminReleaseIpAddress</a> when the user disconnects. Otherwise, RAS does not notify the DLL when this IP address is released.


## -returns



If function succeeds, the return value should be NO_ERROR.

If the function returns anything other than NO_ERROR, RAS will terminate the connection.




## -remarks



RAS supports multiple Administration DLLs. However, RAS calls 
<b>MprAdminGetIpAddressForUser</b> only in the first DLL that implements and export it. RAS ignores implementations of these functions in the other DLLs. RAS checks the DLLs for these functions in the order in which they are listed in the 
<a href="https://msdn.microsoft.com/e83a5e37-a39d-4465-abc9-653cdd56893b">registry</a>.

An administration DLL need not implement the 
<b>MprAdminGetIpAddressForUser</b> function. However, if the DLL implements 
<b>MprAdminGetIpAddressForUser</b>, it must also implement 
<a href="https://msdn.microsoft.com/7a1570a9-b43f-4603-a5ed-6d078a5bbb7c">MprAdminReleaseIpAddress</a>.

Do not call any of the 
<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a> or 
<a href="https://msdn.microsoft.com/e58fa4a6-16d3-4953-bf21-887d08e25af7">RAS User Administration Functions</a> from inside 
<b>MprAdminGetIpAddressForUser</b>. Calls to these functions will not return when made from within a callout function.




## -see-also




<a href="https://msdn.microsoft.com/7a1570a9-b43f-4603-a5ed-6d078a5bbb7c">MprAdminReleaseIpAddress</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

