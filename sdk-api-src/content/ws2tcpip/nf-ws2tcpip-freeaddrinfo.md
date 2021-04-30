---
UID: NF:ws2tcpip.freeaddrinfo
title: freeaddrinfo function (ws2tcpip.h)
description: Frees address information that the getaddrinfo function dynamically allocates in addrinfo structures.
helpviewer_keywords: ["FreeAddrInfoA","_win32_freeaddrinfo_2","freeaddrinfo","freeaddrinfo function [Winsock]","winsock.freeaddrinfo_2","ws2tcpip/freeaddrinfo"]
old-location: winsock\freeaddrinfo_2.htm
tech.root: WinSock
ms.assetid: d2d944df-3773-4918-a89a-3402baf8f5e3
ms.date: 12/05/2018
ms.keywords: FreeAddrInfoA, _win32_freeaddrinfo_2, freeaddrinfo, freeaddrinfo function [Winsock], winsock.freeaddrinfo_2, ws2tcpip/freeaddrinfo
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - freeaddrinfo
 - ws2tcpip/freeaddrinfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - freeaddrinfo
---

# freeaddrinfo function


## -description

The 
<b>freeaddrinfo</b> function frees address information that the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function dynamically allocates in <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structures.

## -parameters

### -param pAddrInfo [in]

A pointer to the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure or linked list of 
<b>addrinfo</b> structures to be freed. All dynamic storage pointed to within the 
<b>addrinfo</b> structure or structures is also freed.

## -returns

This function does not return a value.

## -remarks

The 
<b>freeaddrinfo</b> function frees <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structures dynamically allocated by the ANSI <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function. The <b>freeaddrinfo</b> function frees the initial 
<b>addrinfo</b> structure pointed to in the <i>ai</i> parameter, including any buffers to which structure members point, then continues freeing any 
<b>addrinfo</b> structures linked by the <b>ai_next</b> member of the <b>addrinfo</b> structure. The 
<b>freeaddrinfo</b> function continues freeing linked structures until a <b>NULL</b> <b>ai_next</b> member is encountered.

Macros in the Winsock header file define a mixed-case function name of <b>FreeAddrInfo</b> and an <b>ADDRINFOT</b> structure. This <b>FreeAddrInfo</b> function should be called with the <i>ai</i> parameter of a pointer of type <b>ADDRINFOT</b>. When UNICODE or _UNICODE is not defined, <b>FreeAddrInfo</b> is defined to <b>freeaddrinfo</b>, the ANSI version of the function, and <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure. When UNICODE or _UNICODE is defined, <b>FreeAddrInfo</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfow">FreeAddrInfoW</a>, the Unicode version of the function, and <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structure.

<h3><a id="Support_for_freeaddrinfo_on_earlier_versions_of_Windows_"></a><a id="support_for_freeaddrinfo_on_earlier_versions_of_windows_"></a><a id="SUPPORT_FOR_FREEADDRINFO_ON_EARLIER_VERSIONS_OF_WINDOWS_"></a>Support for freeaddrinfo on earlier versions of Windows
</h3>
The <b>freeaddrinfo</b> function was added to the <i>Ws2_32.dll</i> on Windows XP and later. 

The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfow">FreeAddrInfoW</a> function is the Unicode version of  <b>freeaddrinfo</b>.  The <b>FreeAddrInfoW</b> function was added to the <i>Ws2_32.dll</i> in Windows XP with Service Pack 2 (SP2). The <b>FreeAddrInfoW</b> function cannot be used on versions of Windows earlier than Windows XP with SP2.

<b>Windows Phone 8:</b> The <b>freeaddrinfo</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>freeaddrinfo</b> and  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfow">FreeAddrInfoW</a> functions are supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfow">FreeAddrInfoW</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>