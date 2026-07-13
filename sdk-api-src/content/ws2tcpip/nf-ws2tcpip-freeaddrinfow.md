---
UID: NF:ws2tcpip.FreeAddrInfoW
title: FreeAddrInfoW function (ws2tcpip.h)
description: Frees address information that the GetAddrInfoW function dynamically allocates in addrinfoW structures.
helpviewer_keywords: ["FreeAddrInfoW","FreeAddrInfoW function [Winsock]","winsock.freeaddrinfow","ws2tcpip/FreeAddrInfoW"]
old-location: winsock\freeaddrinfow.htm
tech.root: WinSock
ms.assetid: 0a2a226c-2068-4538-b499-04cfbfd65b8a
ms.date: 12/05/2018
ms.keywords: FreeAddrInfoW, FreeAddrInfoW function [Winsock], winsock.freeaddrinfow, ws2tcpip/FreeAddrInfoW
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeAddrInfoW
 - ws2tcpip/FreeAddrInfoW
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
 - FreeAddrInfoW
---

# FreeAddrInfoW function


## -description

The 
<b>FreeAddrInfoW</b> function frees address information that the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function dynamically allocates in <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structures.

## -parameters

### -param pAddrInfo [in]

A pointer to the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structure or linked list of 
<b>addrinfoW</b> structures to be freed. All dynamic storage pointed to within the 
<b>addrinfoW</b> structure or structures is also freed.

## -returns

This function does not return a value.

## -remarks

The 
<b>FreeAddrInfoW</b> function frees <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structures dynamically allocated by the Unicode <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function. The <b>FreeAddrInfoW</b> function frees the initial 
<b>addrinfoW</b> structure pointed to in the <i>pAddrInfo</i> parameter, including any buffers to which structure members point, then continues freeing any 
<b>addrinfoW</b> structures linked by the <b>ai_next</b> member of the <b>addrinfoW</b> structure. The 
<b>FreeAddrInfoW</b> function continues freeing linked structures until a <b>NULL</b> <b>ai_next</b> member is encountered.

Macros in the Winsock header file define a mixed-case function name of <b>FreeAddrInfo</b> and an <b>ADDRINFOT</b> structure. This <b>FreeAddrInfo</b> function should be called with the <i>pAddrInfo</i> parameter of a pointer of type <b>ADDRINFOT</b>. When UNICODE or _UNICODE is defined, <b>FreeAddrInfo</b> is defined to <b>FreeAddrInfoW</b>, the Unicode version of the function, and <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structure. When UNICODE or _UNICODE is not defined, <b>FreeAddrInfo</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfo">freeaddrinfo</a>, the ANSI version of the function, and <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The ws2tcpip.h header defines FreeAddrInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-freeaddrinfo">freeaddrinfo</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>