---
UID: NF:nspapi.GetNameByTypeW
title: GetNameByTypeW function (nspapi.h)
description: The GetNameByType function retrieves the name of a network service for the specified service type. (Unicode)
helpviewer_keywords: ["GetNameByType", "GetNameByType function [Winsock]", "GetNameByTypeW", "_win32_getnamebytype_2", "nspapi/GetNameByType", "nspapi/GetNameByTypeW", "winsock.getnamebytype_2"]
old-location: winsock\getnamebytype_2.htm
tech.root: WinSock
ms.assetid: 74d747f0-5f5e-4f54-8b2f-7ea96d4043ee
ms.date: 12/05/2018
ms.keywords: GetNameByType, GetNameByType function [Winsock], GetNameByTypeA, GetNameByTypeW, _win32_getnamebytype_2, nspapi/GetNameByType, nspapi/GetNameByTypeA, nspapi/GetNameByTypeW, winsock.getnamebytype_2
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNameByTypeW (Unicode) and GetNameByTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNameByTypeW
 - nspapi/GetNameByTypeW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - GetNameByType
 - GetNameByTypeA
 - GetNameByTypeW
---

# GetNameByTypeW function


## -description

The 
<b>GetNameByType</b> function retrieves the name of a network service for the specified service type.


<div class="alert"><b>Note</b>  The 
<b>GetNameByType</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, the reference material is as follows.</div>
<div> </div>



<div class="alert"><b>Note</b>  The functions detailed in 
<a href="/windows/desktop/WinSock/protocol-independent-name-resolution-2">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2.</div>
<div> </div>

## -parameters

### -param lpServiceType [in]

A pointer to a globally unique identifier (GUID) that specifies the type of the network service. The <i>Svcguid.h</i> header file includes definitions of several GUID service types, and macros for working with them.

The <i>Svcguid.h</i> header file is not automatically included by the <i>Winsock2.h</i> header file.

### -param lpServiceName [out]

A pointer to a buffer to receive a zero-terminated string that uniquely represents the name of the network service.

### -param dwNameLength [in]

A pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpServiceName</i>. On output, the variable contains the actual size of the service name string, in bytes.

## -returns

If the function succeeds, the return value is not SOCKET_ERROR (–1).

If the function fails, the return value is SOCKET_ERROR (–1). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/nspapi/nf-nspapi-gettypebynamea">GetTypeByName</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines GetNameByType as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
