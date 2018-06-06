---
UID: NF:ws2tcpip.FreeAddrInfoW
title: FreeAddrInfoW function
author: windows-sdk-content
description: Frees address information that the GetAddrInfoW function dynamically allocates in addrinfoW structures.
old-location: winsock\freeaddrinfow.htm
old-project: WinSock
ms.assetid: 0a2a226c-2068-4538-b499-04cfbfd65b8a
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: FreeAddrInfoW, FreeAddrInfoW function [Winsock], winsock.freeaddrinfow, ws2tcpip/FreeAddrInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - FreeAddrInfoW
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FreeAddrInfoW function


## -description


The 
<b>FreeAddrInfoW</b> function frees address information that the 
<a href="https://msdn.microsoft.com/82436a88-5b37-4758-a5c9-b60dd1cbc36c">GetAddrInfoW</a> function dynamically allocates in <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures.


## -parameters




### -param pAddrInfo [in]

A pointer to the 
<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure or linked list of 
<b>addrinfoW</b> structures to be freed. All dynamic storage pointed to within the 
<b>addrinfoW</b> structure or structures is also freed.


## -returns



This function does not return a value.




## -remarks



The 
<b>FreeAddrInfoW</b> function frees <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures dynamically allocated by the Unicode <a href="https://msdn.microsoft.com/82436a88-5b37-4758-a5c9-b60dd1cbc36c">GetAddrInfoW</a> function. The <b>FreeAddrInfoW</b> function frees the initial 
<b>addrinfoW</b> structure pointed to in the <i>pAddrInfo</i> parameter, including any buffers to which structure members point, then continues freeing any 
<b>addrinfoW</b> structures linked by the <b>ai_next</b> member of the <b>addrinfoW</b> structure. The 
<b>FreeAddrInfoW</b> function continues freeing linked structures until a <b>NULL</b> <b>ai_next</b> member is encountered.

Macros in the Winsock header file define a mixed-case function name of <b>FreeAddrInfo</b> and an <b>ADDRINFOT</b> structure. This <b>FreeAddrInfo</b> function should be called with the <i>pAddrInfo</i> parameter of a pointer of type <b>ADDRINFOT</b>. When UNICODE or _UNICODE is defined, <b>FreeAddrInfo</b> is defined to <b>FreeAddrInfoW</b>, the Unicode version of the function, and <b>ADDRINFOT</b> is defined to the <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure. When UNICODE or _UNICODE is not defined, <b>FreeAddrInfo</b> is defined to <a href="https://msdn.microsoft.com/d2d944df-3773-4918-a89a-3402baf8f5e3">freeaddrinfo</a>, the ANSI version of the function, and <b>ADDRINFOT</b> is defined to the <a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a> structure.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/82436a88-5b37-4758-a5c9-b60dd1cbc36c">GetAddrInfoW</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>



<a href="https://msdn.microsoft.com/d2d944df-3773-4918-a89a-3402baf8f5e3">freeaddrinfo</a>



<a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a>
 

 

