---
UID: NF:ws2spi.WPUModifyIFSHandle
title: WPUModifyIFSHandle function (ws2spi.h)
description: The WPUModifyIFSHandle function receives a (possibly) modified IFS handle from Ws2_32.dll.
helpviewer_keywords: ["WPUModifyIFSHandle","WPUModifyIFSHandle function [Winsock]","_win32_wpumodifyifshandle_2","winsock.wpumodifyifshandle_2","ws2spi/WPUModifyIFSHandle"]
old-location: winsock\wpumodifyifshandle_2.htm
tech.root: WinSock
ms.assetid: f58971eb-0948-4e16-a767-1d4cba9ec721
ms.date: 12/05/2018
ms.keywords: WPUModifyIFSHandle, WPUModifyIFSHandle function [Winsock], _win32_wpumodifyifshandle_2, winsock.wpumodifyifshandle_2, ws2spi/WPUModifyIFSHandle
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
 - WPUModifyIFSHandle
 - ws2spi/WPUModifyIFSHandle
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
 - WPUModifyIFSHandle
---

# WPUModifyIFSHandle function


## -description

The 
**WPUModifyIFSHandle** function receives a (possibly) modified IFS handle from Ws2_32.dll.

## -parameters

### -param dwCatalogEntryId [in]

Descriptor identifying the calling service provider.

### -param ProposedHandle [in]

IFS handle allocated by the provider.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WPUModifyIFSHandle** returns the modified socket handle. Otherwise, it returns INVALID_SOCKET, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The proposed handle is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
**WPUModifyIFSHandle** handle allows the WS2_32.dll to streamline its internal operations by returning a possibly modified version of the supplied IFS handle. The returned handle is guaranteed to be indistinguishable from the proposed handle as far as the operating system is concerned. IFS providers must call this function before returning any newly created socket descriptor to a service provider. The service provider will only use the modified handle for any subsequent socket operations. This routine is only used by IFS providers whose socket descriptors are real IFS handles.


<div> </div>**Layered Service Provider Considerations**

This procedure may also be used by a layered provider that is layered on top of a base IFS provider and wants to expose the base provider's socket handles as its own instead of creating them with a 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a> call. A layered provider that wishes to "pass through" the IFS socket handles it receives from the next layer in the chain can call 
**WPUModifyIFSHandle**, passing its own catalog entry ID as <i>dwCatalogEntryId</i>. This informs the Windows Sockets DLL that this layer, and not the next layer, should be the target for SPI calls involving that socket handle.

There are several limitations a layered provider should observe if it takes this approach.

 
- The provider should expose base provider entry points for 
[LPWSPSend](nc-ws2spi-lpwspsend.md) and 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md) in the procedure dispatch table it returns at the time of 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> to make sure the Windows Sockets SPI client's access to these functions is as efficient as possible. 
- The provider cannot rely on its 
[LPWSPSend](nc-ws2spi-lpwspsend.md) and 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md) functions being invoked for all I/O, particularly in the case of the I/O system functions <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>. These functions would bypass the layered provider and invoke the base IFS provider's implementation directly even if the layered provider puts its own entry points for these functions into the procedure dispatch table. 
- The provider cannot rely on any ability to post-process overlapped I/O using 
[LPWSPSend](nc-ws2spi-lpwspsend.md), 
[LPWSPSendTo](nc-ws2spi-lpwspsendto.md), 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md), 
[LPWSPRecvFrom](nc-ws2spi-lpwsprecvfrom.md), or 
[LPWSPIoctl](nc-ws2spi-lpwspioctl.md). Post-processing notification may happen through completion ports and bypass the layered provider entirely. A layered provider has no way to determine that a completion port was used or determine what port it is. The layered provider has no way to insert itself into the notification sequence. 
- The provider should pass through all overlapped I/O requests directly to the base provider using the original overlapped parameters (for example, the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure and completion routine pointer). The provider should expose the base provider entry point for 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">WSPGetOverlappedResult</a>. Since some overlapped I/O requests can bypass the layered provider completely, the layered provider cannot reliably mark 
**WSAOVERLAPPED** structures to determine which ones it can report results for, and which ones would have to be passed through to the underlying provider's 
**WSPGetOverlappedResult**. This effectively means that 
[LPWSPIoctl](nc-ws2spi-lpwspioctl.md) has to be a pass-through operation to the underlying provider.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">WSPGetOverlappedResult</a>



[LPWSPIoctl](nc-ws2spi-lpwspioctl.md)



[LPWSPRecv](nc-ws2spi-lpwsprecv.md)



[LPWSPSend](nc-ws2spi-lpwspsend.md)

