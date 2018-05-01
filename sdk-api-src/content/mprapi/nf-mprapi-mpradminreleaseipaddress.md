---
UID: NF:mprapi.MprAdminReleaseIpAddress
title: MprAdminReleaseIpAddress function
author: windows-driver-content
description: The MprAdminReleaseIpAddress function is called when a user disconnects and the user's IP address is about to be released.
old-location: rras\mpradminreleaseipaddress.htm
old-project: RRAS
ms.assetid: 7a1570a9-b43f-4603-a5ed-6d078a5bbb7c
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: MprAdminReleaseIpAddress, MprAdminReleaseIpAddress callback function [RAS], _mpr_mpradminreleaseipaddress, mprapi/MprAdminReleaseIpAddress, rras.mpradminreleaseipaddress
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Mprapi.h
api_name:
-	MprAdminReleaseIpAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminReleaseIpAddress function


## -description


The 
<b>MprAdminReleaseIpAddress</b> function is called when a user disconnects and the user's IP address is about to be released.


## -parameters




### -param lpszUserName

TBD


### -param lpszPortName

TBD


### -param lpdwIpAddress [in]

Pointer to a <b>DWORD</b> variable. This variable specifies the IP address to be released.


#### - lpwszPortName [in]

Pointer to a Unicode string that specifies the name of the port on which the user is attempting to connect.


#### - lpwszUserName [in]

Pointer to a Unicode string that specifies the name of the user that requires an IP address.


## -returns



This function does not have a return value.




## -remarks



An administration DLL need not implement the 
<b>MprAdminReleaseIpAddress</b> function. However, if the DLL implements 
<b>MprAdminReleaseIpAddress</b>, it must also implement 
<a href="https://msdn.microsoft.com/79deeb39-1916-4bb0-b701-8f0a05dc55af">MprAdminGetIpAddressForUser</a>.

RAS supports multiple Administration DLLs. However, RAS calls 
<b>MprAdminReleaseIpAddress</b> only in the first DLL that implements and export it. RAS ignores implementations of these functions in the other DLLs. RAS checks the DLLs for these functions in the order in which they are listed in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926940">registry</a>.

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
 

 

