---
UID: NF:ws2spi.WPUCreateSocketHandle
title: WPUCreateSocketHandle function (ws2spi.h)
description: The WPUCreateSocketHandle function creates a new socket handle.
helpviewer_keywords: ["WPUCreateSocketHandle","WPUCreateSocketHandle function [Winsock]","_win32_wpucreatesockethandle_2","winsock.wpucreatesockethandle_2","ws2spi/WPUCreateSocketHandle"]
old-location: winsock\wpucreatesockethandle_2.htm
tech.root: WinSock
ms.assetid: ecbf9d8b-b705-4160-ac77-afa5b1501534
ms.date: 12/05/2018
ms.keywords: WPUCreateSocketHandle, WPUCreateSocketHandle function [Winsock], _win32_wpucreatesockethandle_2, winsock.wpucreatesockethandle_2, ws2spi/WPUCreateSocketHandle
req.header: ws2spi.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WPUCreateSocketHandle
 - ws2spi/WPUCreateSocketHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUCreateSocketHandle
---

# WPUCreateSocketHandle function


## -description

The 
**WPUCreateSocketHandle** function creates a new socket handle.

## -parameters

### -param dwCatalogEntryId [in]

Descriptor identifying the calling service provider.

### -param dwContext [in]

Context value to associate with the new socket handle.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WPUCreateSocketHandle** returns the new socket handle. Otherwise, it returns INVALID_SOCKET, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
There are not enough buffers available to create the new socket handle.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
**WPUCreateSocketHandle** function creates a new socket handle for the specified provider. The handles created by 
**WPUCreateSocketHandle** are indistinguishable from true file system handles. This is significant in two respects. First, the Windows Socket 2 architecture takes care of redirecting the file system functions <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> to this service provider's 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md) and 
[LPWSPSend](nc-ws2spi-lpwspsend.md) functions, respectively. Second, in operating systems that support completion ports, the Windows Sockets 2 architecture supports associating a completion port with the socket handle and using it to report overlapped I/O completion.


<div class="alert">**Note**  The mechanism for redirecting <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> necessarily involves a user-to-kernel transition to get to the redirector, followed by a kernel-to-user transition to get to 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md) or 
[LPWSPSend](nc-ws2spi-lpwspsend.md). On return, these transitions are retraced in reverse. This can be a significant performance penalty. Any service provider that uses 
**WPUCreateSocketHandle** to create its socket handles should not set XP1_IFS_HANDLES in its 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure. Clients should take the absence of XP1_IFS_HANDLES as guidance to avoid the use of **ReadFile** and **WriteFile**.</div>
<div> </div>
<div class="alert">**Note**  There is no exceptional performance penalty for using the completion port mechanism with socket handles created with 
**WPUCreateSocketHandle**. A service provider should use 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucompleteoverlappedrequest">WPUCompleteOverlappedRequest</a> to announce completion of overlapped I/O operations that may involve a completion port. Clients may freely use operating system functions to create, associate, and use a completion port for completion notification (for example, <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>, <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>, see the relevant operating system documentation for details). Note that completion ports are not integrated with the other asynchronous notification mechanisms offered by Windows Sockets 2. That is, a client can do a multiple-wait that includes multiple events and completion callbacks, but there is no predefined way for the multiple-wait to include completion ports.</div>
<div> </div>



<div> </div>**Layered Service Provider Considerations**

This procedure is of particular interest to Layered Service Providers. A layered service provider may use this procedure, instead of 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a> to create the socket handles it exposes to its client. The advantage of using this procedure is that all I/O requests involving the socket can be guaranteed to go through this service provider. This is true even if the client assumes that the sockets are file system handles and calls the file system functions <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> (although it would pay a performance penalty for this assumption).

The guarantee that all I/O goes through this layer is a requirement for layers that need to process the I/O stream either before or after the actual I/O operation. Creating socket handles using 
**WPUCreateSocketHandle** and specifying an appropriate service provider interface procedure dispatch table at the time of 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> ensures that the layer has the chance to get involved in starting each I/O operation. When the client requests overlapped I/O operations, this service provider layer will usually have to arrange to get into the path of I/O completion notification as well.

To see why this is true, consider what happens if the client associates a completion port with the socket handle for the purpose of overlapped I/O completion notification. The port is associated with the socket handle exposed by this layer, not the next layer's socket handle. There is no way for this layer to determine if a completion port has been associated or what the port is. When this layer calls the next layer's I/O operation, it uses the next layer's socket handle. The next layer's socket handle will not have the same completion port association. The client's expected completion-port notification will not happen without some extra help.

The usual way a layered service provider takes care of this is to substitute a different overlapped I/O structure and different overlapped I/O parameters when invoking an I/O operation in the next layer. The substitute overlapped I/O structure references the client's stored overlapped structure and parameters. The invocation of the next layer sets up a callback notification. When the callback notification occurs, this layer performs any post-processing desired, retrieves the overlapped I/O information it stored on behalf of the client, discards the substitute structures, and forwards an appropriate completion notification to the client.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosesockethandle">WPUCloseSocketHandle</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucompleteoverlappedrequest">WPUCompleteOverlappedRequest</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuquerysockethandlecontext">WPUQuerySocketHandleContext</a>



[LPWSPRecv](nc-ws2spi-lpwsprecv.md)



[LPWSPSend](nc-ws2spi-lpwspsend.md)



<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>

