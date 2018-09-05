---
UID: NF:winsock2.WSACancelBlockingCall
title: WSACancelBlockingCall function
author: windows-sdk-content
description: The WSACancelBlockingCall function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.
old-location: winsock\wsacancelblockingcall_2.htm
old-project: WinSock
ms.assetid: b3597d29-51a5-410f-9925-4d678dd641c1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSACancelBlockingCall, WSACancelBlockingCall function [Winsock], _win32_wsacancelblockingcall_2, winsock.wsacancelblockingcall_2, winsock2/WSACancelBlockingCall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock2.h
api_name:
 - WSACancelBlockingCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSACancelBlockingCall function


## -description


The 
<b>WSACancelBlockingCall</b> function has been removed in compliance with the Windows Sockets 2 specification, revision 2.2.0.

The function is not exported directly by WS2_32.DLL and Windows Sockets 2 applications should not use this function. Windows Sockets 1.1 applications that call this function are still supported through the WINSOCK.DLL and WSOCK32.DLL.

Blocking hooks are generally used to keep a single-threaded GUI application responsive during calls to blocking functions. Instead of using blocking hooks, an applications should use a separate thread (separate from the main GUI thread) for network activity.


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

