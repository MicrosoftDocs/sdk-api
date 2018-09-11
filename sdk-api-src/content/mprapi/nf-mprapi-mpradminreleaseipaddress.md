---
UID: NF:mprapi.MprAdminReleaseIpAddress
title: MprAdminReleaseIpAddress function
author: windows-sdk-content
description: The MprAdminReleaseIpAddress function is called when a user disconnects and the user's IP address is about to be released.
old-location: rras\mpradminreleaseipaddress.htm
tech.root: RRAS
ms.assetid: 7a1570a9-b43f-4603-a5ed-6d078a5bbb7c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MprAdminReleaseIpAddress, MprAdminReleaseIpAddress callback, MprAdminReleaseIpAddress callback function [RAS], _mpr_mpradminreleaseipaddress, mprapi/MprAdminReleaseIpAddress, rras.mpradminreleaseipaddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminReleaseIpAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


## -returns



This function does not have a return value.




## -remarks



An administration DLL need not implement the 
<b>MprAdminReleaseIpAddress</b> function. However, if the DLL implements 
<b>MprAdminReleaseIpAddress</b>, it must also implement 
<a href="https://msdn.microsoft.com/79deeb39-1916-4bb0-b701-8f0a05dc55af">MprAdminGetIpAddressForUser</a>.

RAS supports multiple Administration DLLs. However, RAS calls 
<b>MprAdminReleaseIpAddress</b> only in the first DLL that implements and export it. RAS ignores implementations of these functions in the other DLLs. RAS checks the DLLs for these functions in the order in which they are listed in the 
<a href="https://msdn.microsoft.com/e83a5e37-a39d-4465-abc9-653cdd56893b">registry</a>.

<b>Windows 2000 Server or earlier:  </b>If RAS does not accept the new link, RAS does not call the 
<a href="https://msdn.microsoft.com/7f2b30e8-ba1d-4db3-843f-f9eafca47add">MprAdminLinkHangupNotification</a> function.

Do not call any of the 
<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a> or 
<a href="https://msdn.microsoft.com/e58fa4a6-16d3-4953-bf21-887d08e25af7">RAS User Administration Functions</a> from inside 
<b>MprAdminReleaseIpAddress</b>. Calls to these functions do not return when made from within a callout function.




## -see-also




<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/79deeb39-1916-4bb0-b701-8f0a05dc55af">MprAdminGetIpAddressForUser</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

