---
UID: NF:winsock2.WSASetBlockingHook
title: WSASetBlockingHook function (winsock2.h)
author: windows-sdk-content
description: This function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.
old-location: winsock\wsasetblockinghook_2.htm
tech.root: WinSock
ms.assetid: 3a420778-0082-4c81-bdc9-d79c67453fae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSASetBlockingHook, WSASetBlockingHook function [Winsock], _win32_wsasetblockinghook_2, winsock.wsasetblockinghook_2, winsock2/WSASetBlockingHook
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock2.h
api_name:
 - WSASetBlockingHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSASetBlockingHook function


## -description


This function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.

The function is not exported directly by WS2_32.DLL, and Windows Sockets 2 applications should not use this function. Windows Sockets 1.1 applications that call this function are still supported through the WINSOCK.DLL and WSOCK32.DLL.

Blocking hooks are generally used to keep a single-threaded GUI application responsive during calls to blocking functions. Instead of using blocking hooks, an application should use a separate thread (separate from the main GUI thread) for network activity.


## -parameters




### -param lpBlockFunc


## -see-also




<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

