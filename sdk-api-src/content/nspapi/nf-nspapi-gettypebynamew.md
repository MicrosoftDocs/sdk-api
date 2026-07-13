---
UID: NF:nspapi.GetTypeByNameW
title: GetTypeByNameW function (nspapi.h)
description: The GetTypeByName function retrieves a service type GUID for a network service specified by name. (Unicode)
helpviewer_keywords: ["GetTypeByName", "GetTypeByName function [Winsock]", "GetTypeByNameW", "_win32_gettypebyname_2", "nspapi/GetTypeByName", "nspapi/GetTypeByNameW", "winsock.gettypebyname_2"]
old-location: winsock\gettypebyname_2.htm
tech.root: WinSock
ms.assetid: 177bbae5-bc00-4ce5-a0f7-8474f0c2cb2e
ms.date: 12/05/2018
ms.keywords: GetTypeByName, GetTypeByName function [Winsock], GetTypeByNameA, GetTypeByNameW, _win32_gettypebyname_2, nspapi/GetTypeByName, nspapi/GetTypeByNameA, nspapi/GetTypeByNameW, winsock.gettypebyname_2
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTypeByNameW (Unicode) and GetTypeByNameA (ANSI)
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
 - GetTypeByNameW
 - nspapi/GetTypeByNameW
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
 - GetTypeByName
 - GetTypeByNameA
 - GetTypeByNameW
---

# GetTypeByNameW function


## -description

The 
<b>GetTypeByName</b> function retrieves a service type <b>GUID</b> for a network service specified by name.


<div class="alert"><b>Note</b>  The 
<b>GetTypeByName</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, this reference material is included. The functions detailed in 
<a href="/windows/desktop/WinSock/protocol-independent-name-resolution-2">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2.</div>
<div> </div>

## -parameters

### -param lpServiceName [in]

A pointer to a zero-terminated string that uniquely represents the name of the service. For example, "MY SNA SERVER."

### -param lpServiceType [in, out]

A pointer to a variable to receive a globally unique identifier (<b>GUID</b>) that specifies the type of the network service. The <i>Svcguid.h</i> header file includes definitions of several <b>GUID</b> service types and macros for working with them.

The <i>Svcguid.h</i> header file is not automatically included by the <i>Winsock2.h</i> header file.

## -returns

If the function succeeds, the return value is zero.

If the function fails, the return value is SOCKET_ERROR( – 1). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns the following extended error value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified service type is unknown.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/nspapi/nf-nspapi-getnamebytypea">GetNameByType</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines GetTypeByName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
