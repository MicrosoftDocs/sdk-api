---
UID: NS:winsock2._WSAServiceClassInfoW
title: "_WSAServiceClassInfoW"
author: windows-sdk-content
description: The WSASERVICECLASSINFO structure contains information about a specified service class. For each service class in Windows Sockets 2, there is a single WSASERVICECLASSINFO structure.
old-location: winsock\wsaserviceclassinfo_2.htm
old-project: winsock
ms.assetid: 02422c24-34a6-4e34-a795-66b0b687ac44
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPWSASERVICECLASSINFOW, *PWSASERVICECLASSINFOW, PWSASERVICECLASSINFOW, PWSASERVICECLASSINFOW structure pointer [Winsock], WSASERVICECLASSINFO, WSASERVICECLASSINFO structure [Winsock], WSASERVICECLASSINFOA, WSASERVICECLASSINFOW, _WSAServiceClassInfoW, _win32_wsaserviceclassinfo_2, winsock.wsaserviceclassinfo_2, winsock2/PWSASERVICECLASSINFOW, winsock2/WSASERVICECLASSINFO, winsock2/WSASERVICECLASSINFOA, winsock2/WSASERVICECLASSINFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WSASERVICECLASSINFOW, *PWSASERVICECLASSINFOW, *LPWSASERVICECLASSINFOW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSAServiceClassInfoW structure


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

Array of <a href="https://msdn.microsoft.com/b4f811ad-7967-45bd-b563-a28bb1633596">WSANSCLASSINFO</a> structures that contains information about the service class.


## -see-also




<a href="https://msdn.microsoft.com/babe1c96-9077-4d91-a52a-839c89d7a83b">NSPGetServiceClassInfo</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>
 

 

