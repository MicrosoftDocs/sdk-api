---
UID: NS:winsock2._WSAOVERLAPPED
title: WSAOVERLAPPED (winsock2.h)
description: Provides a communication medium between the initiation of an overlapped I/O operation and its subsequent completion.
helpviewer_keywords: ["*LPWSAOVERLAPPED","LPWSAOVERLAPPED","LPWSAOVERLAPPED structure pointer [Winsock]","WSAOVERLAPPED","WSAOVERLAPPED structure [Winsock]","_win32_wsaoverlapped_2","winsock.wsaoverlapped_2","winsock2/LPWSAOVERLAPPED","winsock2/WSAOVERLAPPED"]
old-location: winsock\wsaoverlapped_2.htm
tech.root: WinSock
ms.assetid: 91004241-e0ea-4bda-a0f5-71688ac83038
ms.date: 12/05/2018
ms.keywords: '*LPWSAOVERLAPPED, LPWSAOVERLAPPED, LPWSAOVERLAPPED structure pointer [Winsock], WSAOVERLAPPED, WSAOVERLAPPED structure [Winsock], _win32_wsaoverlapped_2, winsock.wsaoverlapped_2, winsock2/LPWSAOVERLAPPED, winsock2/WSAOVERLAPPED'
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
req.typenames: WSAOVERLAPPED, *LPWSAOVERLAPPED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAOVERLAPPED
 - winsock2/_WSAOVERLAPPED
 - LPWSAOVERLAPPED
 - winsock2/LPWSAOVERLAPPED
 - WSAOVERLAPPED
 - winsock2/WSAOVERLAPPED
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
 - WSAOVERLAPPED
---

# WSAOVERLAPPED structure


## -description

The 
<b>WSAOVERLAPPED</b> structure provides a communication medium between the initiation of an overlapped I/O operation and its subsequent completion. The 
<b>WSAOVERLAPPED</b> structure is compatible with the Windows 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

## -struct-fields

### -field Internal

Type: <b>ULONG_PTR</b>

Reserved for internal use. The Internal member is used internally by the entity that implements overlapped I/O. For service providers that create sockets as installable file system (IFS) handles, this parameter is used by the underlying operating system. Other service providers (non-IFS providers) are free to use this parameter as necessary.

### -field InternalHigh

Type: <b>ULONG_PTR</b>

Reserved. Used internally by the entity that implements overlapped I/O. For service providers that create sockets as IFS handles, this parameter is used by the underlying operating system. NonIFS providers are free to use this parameter as necessary.

### -field Offset

Type: <b>DWORD</b>

Reserved for use by service providers.

### -field OffsetHigh

Type: <b>DWORD</b>

Reserved for use by service providers.

### -field hEvent

Type: <b>HANDLE</b>

If an overlapped I/O operation is issued without an I/O completion routine (the operation's <i>lpCompletionRoutine</i> parameter is set to null), then this parameter should either contain a valid handle to a WSAEVENT object or be null. If the <i>lpCompletionRoutine</i> parameter of the call is non-null then applications are free to use this parameter as necessary.


#### - Pointer

Type: <b>PVOID</b>

Reserved for use by service providers.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup">WSACleanup</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>