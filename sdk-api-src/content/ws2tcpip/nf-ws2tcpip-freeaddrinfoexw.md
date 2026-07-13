---
UID: NF:ws2tcpip.FreeAddrInfoExW
title: FreeAddrInfoExW function (ws2tcpip.h)
description: The FreeAddrInfoExW (Unicode) function (ws2tcpip.h) frees address information that the GetAddrInfoEx function dynamically allocates in addrinfoex structures.
helpviewer_keywords: ["FreeAddrInfoEx","FreeAddrInfoEx function [Winsock]","FreeAddrInfoExW","winsock.freeaddrinfoex","ws2tcpip/FreeAddrInfoEx","ws2tcpip/FreeAddrInfoExW"]
old-location: winsock\freeaddrinfoex.htm
tech.root: WinSock
ms.assetid: bc3d7ba7-ec00-4ee0-ad7d-d46641043a7b
ms.date: 08/16/2022
ms.keywords: FreeAddrInfoEx, FreeAddrInfoEx function [Winsock], FreeAddrInfoExW, winsock.freeaddrinfoex, ws2tcpip/FreeAddrInfoEx, ws2tcpip/FreeAddrInfoExW
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FreeAddrInfoExW (Unicode) and FreeAddrInfoEx (ANSI)
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
 - FreeAddrInfoExW
 - ws2tcpip/FreeAddrInfoExW
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
 - FreeAddrInfoEx
 - FreeAddrInfoEx
 - FreeAddrInfoExW
---

# FreeAddrInfoExW function


## -description

The 
<b>FreeAddrInfoEx</b> function frees address information that the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function dynamically allocates in <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structures.

## -parameters

### -param pAddrInfoEx [in]

A pointer to the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure or linked list of 
<b>addrinfoex</b> structures to be freed. All dynamic storage pointed to within the 
<b>addrinfoex</b> structure or structures is also freed.

## -returns

This function does not return a value.

## -remarks

The 
<b>FreeAddrInfoEx</b> function frees <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structures dynamically allocated by the  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function. The <b>FreeAddrInfoEx</b> function frees the initial 
<b>addrinfoex</b> structure pointed to in the <i>pAddrInfo</i> parameter, including any buffers to which structure members point, then continues freeing any 
<b>addrinfoex</b> structures linked by the <b>ai_next</b> member of the <b>addrinfoex</b> structure. The 
<b>FreeAddrInfoEx</b> function continues freeing linked structures until a <b>NULL</b> <b>ai_next</b> member is encountered.

When UNICODE or _UNICODE is defined, <b>FreeAddrInfoEx</b> is defined to <b>FreeAddrInfoExW</b>, the Unicode version of the function, and <b>ADDRINFOEX</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoexW</a> structure. When UNICODE or _UNICODE is not defined, <b>FreeAddrInfoEx</b> is defined to <b>FreeAddrInfoExA</b>, the ANSI version of the function, and <b>ADDRINFOEX</b> is defined to the <b>addrinfoexA</b> structure. 

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>FreeAddrInfoExW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The ws2tcpip.h header defines FreeAddrInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a>
