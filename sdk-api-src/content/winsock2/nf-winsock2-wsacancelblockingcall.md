---
UID: NF:winsock2.WSACancelBlockingCall
title: WSACancelBlockingCall function (winsock2.h)
description: The WSACancelBlockingCall function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.
helpviewer_keywords: ["WSACancelBlockingCall","WSACancelBlockingCall function [Winsock]","_win32_wsacancelblockingcall_2","winsock.wsacancelblockingcall_2","winsock2/WSACancelBlockingCall"]
old-location: winsock\wsacancelblockingcall_2.htm
tech.root: WinSock
ms.assetid: b3597d29-51a5-410f-9925-4d678dd641c1
ms.date: 12/05/2018
ms.keywords: WSACancelBlockingCall, WSACancelBlockingCall function [Winsock], _win32_wsacancelblockingcall_2, winsock.wsacancelblockingcall_2, winsock2/WSACancelBlockingCall
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
 - WSACancelBlockingCall
 - winsock2/WSACancelBlockingCall
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
 - WSACancelBlockingCall
---

# WSACancelBlockingCall function


## -description

The 
<b>WSACancelBlockingCall</b> function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.

The function is not exported directly by WS2_32.DLL and Windows Sockets 2 applications should not use this function. Windows Sockets 1.1 applications that call this function are still supported through the WINSOCK.DLL and WSOCK32.DLL.

Blocking hooks are generally used to keep a single-threaded GUI application responsive during calls to blocking functions. Instead of using blocking hooks, an applications should use a separate thread (separate from the main GUI thread) for network activity.



## -see-also

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
