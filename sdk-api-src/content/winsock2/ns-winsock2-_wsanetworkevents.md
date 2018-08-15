---
UID: NS:winsock2._WSANETWORKEVENTS
title: "_WSANETWORKEVENTS"
author: windows-sdk-content
description: The WSANETWORKEVENTS structure is used to store a socket's internal information about network events.
old-location: winsock\wsanetworkevents_2.htm
old-project: winsock
ms.assetid: 72ae4aa8-4e15-4215-8dcb-45e394ac1313
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPWSANETWORKEVENTS, LPWSANETWORKEVENTS, LPWSANETWORKEVENTS structure pointer [Winsock], WSANETWORKEVENTS, WSANETWORKEVENTS structure [Winsock], _WSANETWORKEVENTS, _win32_wsanetworkevents_2, winsock.wsanetworkevents_2, winsock2/LPWSANETWORKEVENTS, winsock2/WSANETWORKEVENTS"
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
req.typenames: WSANETWORKEVENTS, *LPWSANETWORKEVENTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSANETWORKEVENTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSANETWORKEVENTS structure


## -description


The 
<b>WSANETWORKEVENTS</b> structure is used to store a socket's internal information about network events.


## -struct-fields




### -field lNetworkEvents

Indicates which of the FD_XXX network events have occurred.


### -field iErrorCode

Array that contains any associated error codes, with an array index that corresponds to the position of event bits in <b>lNetworkEvents</b>. The identifiers FD_READ_BIT, FD_WRITE_BIT and others can be used to index the <b>iErrorCode</b> array.


## -see-also




<a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>
 

 

