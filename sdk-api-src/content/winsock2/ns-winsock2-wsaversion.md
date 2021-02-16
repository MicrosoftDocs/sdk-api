---
UID: NS:winsock2._WSAVersion
title: WSAVERSION (winsock2.h)
description: The WSAVERSION structure provides version comparison in Windows Sockets.
helpviewer_keywords: ["*LPWSAVERSION","*PWSAVERSION","LPWSAVERSION","LPWSAVERSION structure pointer [Winsock]","PWSAVERSION","PWSAVERSION structure pointer [Winsock]","WSAVERSION","WSAVERSION structure [Winsock]","_win32_wsaversion_2","winsock.wsaversion_2","winsock2/LPWSAVERSION","winsock2/PWSAVERSION","winsock2/WSAVERSION"]
old-location: winsock\wsaversion_2.htm
tech.root: WinSock
ms.assetid: 27af3b20-9460-466d-bc58-5e31e08bb6c8
ms.date: 12/05/2018
ms.keywords: '*LPWSAVERSION, *PWSAVERSION, LPWSAVERSION, LPWSAVERSION structure pointer [Winsock], PWSAVERSION, PWSAVERSION structure pointer [Winsock], WSAVERSION, WSAVERSION structure [Winsock], _win32_wsaversion_2, winsock.wsaversion_2, winsock2/LPWSAVERSION, winsock2/PWSAVERSION, winsock2/WSAVERSION'
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
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAVersion
 - winsock2/_WSAVersion
 - PWSAVERSION
 - winsock2/PWSAVERSION
 - WSAVERSION
 - winsock2/WSAVERSION
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
 - WSAVERSION
---

# WSAVERSION structure


## -description

The 
<b>WSAVERSION</b> structure provides version comparison in Windows Sockets.

## -struct-fields

### -field dwVersion

Version of Windows Sockets.

### -field ecHow

<a href="/windows/desktop/api/winsock2/ne-winsock2-wsaecomparator">WSAECOMPARATOR</a> enumeration, used in the comparison.

## -see-also

<a href="/windows/desktop/api/winsock2/ne-winsock2-wsaecomparator">WSAECOMPARATOR</a>