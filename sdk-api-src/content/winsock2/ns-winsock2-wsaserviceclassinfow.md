---
UID: NS:winsock2._WSAServiceClassInfoW
title: WSASERVICECLASSINFOW (winsock2.h)
description: The WSASERVICECLASSINFO structure contains information about a specified service class. For each service class in Windows Sockets 2, there is a single WSASERVICECLASSINFO structure. (Unicode)
helpviewer_keywords: ["*LPWSASERVICECLASSINFOW","*PWSASERVICECLASSINFOW","PWSASERVICECLASSINFOW","PWSASERVICECLASSINFOW structure pointer [Winsock]","WSASERVICECLASSINFO","WSASERVICECLASSINFO structure [Winsock]","WSASERVICECLASSINFOA","WSASERVICECLASSINFOW","_win32_wsaserviceclassinfo_2","winsock.wsaserviceclassinfo_2","winsock2/PWSASERVICECLASSINFOW","winsock2/WSASERVICECLASSINFO","winsock2/WSASERVICECLASSINFOA","winsock2/WSASERVICECLASSINFOW"]
old-location: winsock\wsaserviceclassinfo_2.htm
tech.root: WinSock
ms.assetid: 02422c24-34a6-4e34-a795-66b0b687ac44
ms.date: 12/05/2018
ms.keywords: '*LPWSASERVICECLASSINFOW, *PWSASERVICECLASSINFOW, PWSASERVICECLASSINFOW, PWSASERVICECLASSINFOW structure pointer [Winsock], WSASERVICECLASSINFO, WSASERVICECLASSINFO structure [Winsock], WSASERVICECLASSINFOA, WSASERVICECLASSINFOW, _win32_wsaserviceclassinfo_2, winsock.wsaserviceclassinfo_2, winsock2/PWSASERVICECLASSINFOW, winsock2/WSASERVICECLASSINFO, winsock2/WSASERVICECLASSINFOA, winsock2/WSASERVICECLASSINFOW'
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSASERVICECLASSINFOW (Unicode) and WSASERVICECLASSINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSASERVICECLASSINFOW, *PWSASERVICECLASSINFOW, *LPWSASERVICECLASSINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAServiceClassInfoW
 - winsock2/_WSAServiceClassInfoW
 - PWSASERVICECLASSINFOW
 - winsock2/PWSASERVICECLASSINFOW
 - WSASERVICECLASSINFOW
 - winsock2/WSASERVICECLASSINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSASERVICECLASSINFO
 - WSASERVICECLASSINFOA
 - WSASERVICECLASSINFOW
---

# WSASERVICECLASSINFOW structure


## -description

The 
<b>WSASERVICECLASSINFO</b> structure contains information about a specified service class. For each service class in Windows Sockets 2, there is a single 
<b>WSASERVICECLASSINFO</b> structure.

## -struct-fields

### -field lpServiceClassId

Unique Identifier (GUID) for the service class.

### -field lpszServiceClassName

Well known name associated with the service class.

### -field dwCount

Number of entries in <b>lpClassInfos</b>.

### -field lpClassInfos

Array of <a href="/windows/desktop/api/winsock2/ns-winsock2-wsansclassinfow">WSANSCLASSINFO</a> structures that contains information about the service class.

## -see-also

<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspgetserviceclassinfo">NSPGetServiceClassInfo</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>

## -remarks

> [!NOTE]
> The winsock2.h header defines WSASERVICECLASSINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
