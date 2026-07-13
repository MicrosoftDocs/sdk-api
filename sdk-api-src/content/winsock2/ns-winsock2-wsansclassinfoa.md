---
UID: NS:winsock2._WSANSClassInfoA
title: WSANSCLASSINFOA (winsock2.h)
description: The WSANSCLASSINFO structure provides individual parameter information for a specific Windows Sockets namespace. (ANSI)
helpviewer_keywords: ["*LPWSANSCLASSINFOA","*PWSANSCLASSINFO","*LPWSANSCLASSINFO","*PWSANSCLASSINFO","*LPWSANSCLASSINFO structure [Winsock]","*PWSANSCLASSINFOA","WSANSCLASSINFO","WSANSCLASSINFO structure [Winsock]","WSANSCLASSINFOA","winsock.wsansclassinfo","winsock2/*PWSANSCLASSINFO","*LPWSANSCLASSINFO","winsock2/WSANSCLASSINFO"]
old-location: winsock\wsansclassinfo.htm
tech.root: WinSock
ms.assetid: b4f811ad-7967-45bd-b563-a28bb1633596
ms.date: 12/05/2018
ms.keywords: '*LPWSANSCLASSINFOA, *PWSANSCLASSINFO,*LPWSANSCLASSINFO, *PWSANSCLASSINFO,*LPWSANSCLASSINFO structure [Winsock], *PWSANSCLASSINFOA, WSANSCLASSINFO, WSANSCLASSINFO structure [Winsock], WSANSCLASSINFOA, winsock.wsansclassinfo, winsock2/*PWSANSCLASSINFO,*LPWSANSCLASSINFO, winsock2/WSANSCLASSINFO'
req.header: winsock2.h
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
targetos: Windows
req.typenames: WSANSCLASSINFOA, *PWSANSCLASSINFOA, *LPWSANSCLASSINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSANSClassInfoA
 - winsock2/_WSANSClassInfoA
 - PWSANSCLASSINFOA
 - winsock2/PWSANSCLASSINFOA
 - WSANSCLASSINFOA
 - winsock2/WSANSCLASSINFOA
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
 - WSANSCLASSINFO
---

# WSANSCLASSINFOA structure


## -description

The <b>WSANSCLASSINFO</b> structure provides individual parameter information for a specific Windows Sockets namespace.

## -struct-fields

### -field lpszName

String value associated with the parameter, such as SAPID, TCPPORT, and so forth.

### -field dwNameSpace

GUID associated with the namespace.

### -field dwValueType

Value type for the parameter, such as REG_DWORD or REG_SZ, and so forth.

### -field dwValueSize

Size of the parameter provided in <b>lpValue</b>, in bytes.

### -field lpValue

Pointer to the value of the parameter.

## -remarks

The <b>WSANSCLASSINFO</b> structure is defined differently depending on whether ANSI or UNICODE is used. The above syntax block applies to ANSI; for UNICODE, the datatype for <b>lpszName</b> is <b>LPWSTR</b>.





> [!NOTE]
> The winsock2.h header defines WSANSCLASSINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFO</a>
