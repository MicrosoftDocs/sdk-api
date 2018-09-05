---
UID: NS:winsock2._WSANSClassInfoW
title: "_WSANSClassInfoW"
author: windows-sdk-content
description: The WSANSCLASSINFO structure provides individual parameter information for a specific Windows Sockets namespace.
old-location: winsock\wsansclassinfo.htm
old-project: WinSock
ms.assetid: b4f811ad-7967-45bd-b563-a28bb1633596
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPWSANSCLASSINFOW, *PWSANSCLASSINFO,*LPWSANSCLASSINFO, *PWSANSCLASSINFO,*LPWSANSCLASSINFO structure [Winsock], *PWSANSCLASSINFOW, WSANSCLASSINFO, WSANSCLASSINFO structure [Winsock], WSANSCLASSINFOW, _WSANSClassInfoW, winsock.wsansclassinfo, winsock2/*PWSANSCLASSINFO,*LPWSANSCLASSINFO, winsock2/WSANSCLASSINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsock2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WSANSCLASSINFOW, *PWSANSCLASSINFOW, *LPWSANSCLASSINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSANSCLASSINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSANSClassInfoW structure


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




## -see-also




<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFO</a>
 

 

