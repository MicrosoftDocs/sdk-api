---
UID: NF:ws2spi.WPUQueryBlockingCallback
title: WPUQueryBlockingCallback function (ws2spi.h)
description: The WPUQueryBlockingCallback function returns a pointer to a callback function the service provider should invoke periodically while servicing blocking operations.
helpviewer_keywords: ["WPUQueryBlockingCallback","WPUQueryBlockingCallback function [Winsock]","_win32_wpuqueryblockingcallback_2","winsock.wpuqueryblockingcallback_2","ws2spi/WPUQueryBlockingCallback"]
old-location: winsock\wpuqueryblockingcallback_2.htm
tech.root: WinSock
ms.assetid: 08e6215c-536f-4ab2-9d34-096b919ef0be
ms.date: 12/05/2018
ms.keywords: WPUQueryBlockingCallback, WPUQueryBlockingCallback function [Winsock], _win32_wpuqueryblockingcallback_2, winsock.wpuqueryblockingcallback_2, ws2spi/WPUQueryBlockingCallback
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
 - WPUQueryBlockingCallback
 - ws2spi/WPUQueryBlockingCallback
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
 - WPUQueryBlockingCallback
---

# WPUQueryBlockingCallback function


## -description

The 
**WPUQueryBlockingCallback** function returns a pointer to a callback function the service provider should invoke periodically while servicing blocking operations.

## -parameters

### -param dwCatalogEntryId [in]

Descriptor identifying the calling service provider.

### -param lplpfnCallback [out]

Pointer that receives the blocking callback function.

### -param lpdwContext [out]

Pointer that receives a context value that the service provider must pass into the blocking callback.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WPUQueryBlockingCallback** returns zero and stores a pointer to a blocking callback function in <i>lpfnCallback</i> and an associated context value in <i>lpdwContext</i>. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpfnCallback</i> or the <i>lpdwContext</i> parameter is not a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>dwCatalogEntryId</i> parameter is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
**WPUQueryBlockingCallback** function returns a pointer to a callback function in <i>lpfnCallback</i> to be invoked periodically during blocking operations. This function also returns a context value in <i>lpdwContext</i> to be passed into the blocking callback.

In Windows, this function can return null in <i>lpfnCallback</i>, indicating that no user defined–blocking hook is installed. In this case, the service provider should use the native Windows synchronization objects to implement blocking.

LPBLOCKINGCALLBACK is defined as follows:


```cpp
typedef BOOL ( CALLBACK FAR * LPBLOCKINGCALLBACK )( DWORD dwContext );

```


The blocking callback will return **TRUE** if the service provider is to continue waiting for the blocking operation to complete. It will return **FALSE** if the blocking operation has been canceled with the 
<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">WSPCancelBlockingCall</a>.

Any missing components of the address will default to a reasonable value if possible. For example, a missing port number will default to zero.

## -see-also

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">WSPCancelBlockingCall</a>

