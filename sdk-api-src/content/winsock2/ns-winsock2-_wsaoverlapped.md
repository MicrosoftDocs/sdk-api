---
UID: NS:winsock2._WSAOVERLAPPED
title: "_WSAOVERLAPPED"
author: windows-sdk-content
description: Provides a communication medium between the initiation of an overlapped I/O operation and its subsequent completion.
old-location: winsock\wsaoverlapped_2.htm
tech.root: winsock
ms.assetid: 91004241-e0ea-4bda-a0f5-71688ac83038
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPWSAOVERLAPPED, LPWSAOVERLAPPED, LPWSAOVERLAPPED structure pointer [Winsock], WSAOVERLAPPED, WSAOVERLAPPED structure [Winsock], _WSAOVERLAPPED, _win32_wsaoverlapped_2, winsock.wsaoverlapped_2, winsock2/LPWSAOVERLAPPED, winsock2/WSAOVERLAPPED"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSAOVERLAPPED
product: Windows
targetos: Windows
req.typenames: WSAOVERLAPPED, *LPWSAOVERLAPPED
req.redist: 
---

# _WSAOVERLAPPED structure


## -description


The 
<b>WSAOVERLAPPED</b> structure provides a communication medium between the initiation of an overlapped I/O operation and its subsequent completion. The 
<b>WSAOVERLAPPED</b> structure is compatible with the Windows 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.


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




<a href="https://msdn.microsoft.com/72b7cc3e-be34-41e7-acbf-61742149ec8b">WSACleanup</a>



<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>



<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>



<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>
 

 

