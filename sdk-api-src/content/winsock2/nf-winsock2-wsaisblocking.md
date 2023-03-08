---
UID: NF:winsock2.WSAIsBlocking
title: WSAIsBlocking function (winsock2.h)
description: This function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0. (WSAIsBlocking)
helpviewer_keywords: ["WSAIsBlocking","WSAIsBlocking function [Winsock]","_win32_wsaisblocking_2","winsock.wsaisblocking_2","winsock2/WSAIsBlocking"]
old-location: winsock\wsaisblocking_2.htm
tech.root: WinSock
ms.assetid: 2721fb73-4c2e-43c4-aea8-232ba531122f
ms.date: 12/05/2018
ms.keywords: WSAIsBlocking, WSAIsBlocking function [Winsock], _win32_wsaisblocking_2, winsock.wsaisblocking_2, winsock2/WSAIsBlocking
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
 - WSAIsBlocking
 - winsock2/WSAIsBlocking
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
 - WSAIsBlocking
---

# WSAIsBlocking function


## -description

This function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.

The Windows Socket 
<b>WSAIsBlocking</b> function is not exported directly by WS2_32.DLL, and Windows Sockets 2 applications should not use this function. Windows Sockets 1.1 applications that call this function are still supported through the WINSOCK.DLL and WSOCK32.DLL.

Blocking hooks are generally used to keep a single-threaded GUI application responsive during calls to blocking functions. Instead of using blocking hooks, an applications should use a separate thread (separate from the main GUI thread) for network activity.



## -see-also

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
