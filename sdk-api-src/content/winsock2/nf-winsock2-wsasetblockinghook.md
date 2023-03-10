---
UID: NF:winsock2.WSASetBlockingHook
title: WSASetBlockingHook function (winsock2.h)
description: This function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0. (WSASetBlockingHook)
helpviewer_keywords: ["WSASetBlockingHook","WSASetBlockingHook function [Winsock]","_win32_wsasetblockinghook_2","winsock.wsasetblockinghook_2","winsock2/WSASetBlockingHook"]
old-location: winsock\wsasetblockinghook_2.htm
tech.root: WinSock
ms.assetid: 3a420778-0082-4c81-bdc9-d79c67453fae
ms.date: 12/05/2018
ms.keywords: WSASetBlockingHook, WSASetBlockingHook function [Winsock], _win32_wsasetblockinghook_2, winsock.wsasetblockinghook_2, winsock2/WSASetBlockingHook
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSASetBlockingHook
 - winsock2/WSASetBlockingHook
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock2.h
api_name:
 - WSASetBlockingHook
---

# WSASetBlockingHook function


## -description

This function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.

The function is not exported directly by WS2_32.DLL, and Windows Sockets 2 applications should not use this function. Windows Sockets 1.1 applications that call this function are still supported through the WINSOCK.DLL and WSOCK32.DLL.

Blocking hooks are generally used to keep a single-threaded GUI application responsive during calls to blocking functions. Instead of using blocking hooks, an application should use a separate thread (separate from the main GUI thread) for network activity.

## -parameters

### -param lpBlockFunc

## -see-also

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
