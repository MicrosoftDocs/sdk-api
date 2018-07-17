---
UID: NF:ws2tcpip.setsourcefilter
title: setsourcefilter function
author: windows-sdk-content
description: Sets the multicast filter state for an IPv4 or IPv6 socket.
old-location: winsock\setsourcefilter.htm
old-project: winsock
ms.assetid: 320455F3-FDFB-46C6-9F26-3C60064A2CB0
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: setsourcefilter, setsourcefilter function [Winsock], winsock.setsourcefilter, ws2tcpip/setsourcefilter
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
 - setsourcefilter
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# setsourcefilter function


## -description


The 
<b>setsourcefilter</b> inline function  sets the multicast filter state for an IPv4 or IPv6   socket.


## -parameters




### -param Socket [in]

A descriptor that identifies a multicast socket.


### -param Interface [in]

The interface index of the multicast interface.


### -param Group [in]

A pointer to the socket address of the multicast group.


### -param GroupLength [in]

The length, in bytes, of the socket address pointed to by the <i>Group</i> parameter.


### -param FilterMode [in]

The multicast filter mode for the multicast group address.


### -param SourceCount [in]

The number of source addresses in the buffer pointed to by the <i>SourceList</i> parameter.


### -param SourceList [in]

A pointer to a buffer with the  IP addresses to associate with the multicast filter.


## -returns



On success,  <b>setsourcefilter</b> returns NO_ERROR (0). Any nonzero return value indicates failure and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
</table>
 




## -remarks



The 
<b>setsourcefilter</b> inline function is used to set the multicast filter state for an IPv4  or IPv6 socket.

This function is part of socket interface extensions for multicast source filters defined in RFC 3678. An app can  use these functions to retrieve and set the multicast source address filters associated with a socket. 

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/7ca9cb9b-618a-4e73-9e2a-18e55e5c00c0">MULTICAST_MODE_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>



<a href="https://msdn.microsoft.com/17D35D24-C419-4787-AB93-E6B1B6B13807">getipv4sourcefilter</a>



<a href="https://msdn.microsoft.com/2CA84000-F114-439D-BEDE-9990044C7785">getsourcefilter</a>



<a href="https://msdn.microsoft.com/C296D050-9195-42B5-8EBE-C6004F2DA855">setipv4sourcefilter</a>
 

 

