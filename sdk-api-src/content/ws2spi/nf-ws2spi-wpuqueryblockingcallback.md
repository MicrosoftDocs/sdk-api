---
UID: NF:ws2spi.WPUQueryBlockingCallback
title: WPUQueryBlockingCallback function
author: windows-sdk-content
description: The WPUQueryBlockingCallback function returns a pointer to a callback function the service provider should invoke periodically while servicing blocking operations.
old-location: winsock\wpuqueryblockingcallback_2.htm
tech.root: WinSock
ms.assetid: 08e6215c-536f-4ab2-9d34-096b919ef0be
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WPUQueryBlockingCallback, WPUQueryBlockingCallback function [Winsock], _win32_wpuqueryblockingcallback_2, winsock.wpuqueryblockingcallback_2, ws2spi/WPUQueryBlockingCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUQueryBlockingCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WPUQueryBlockingCallback function


## -description


The 
<b>WPUQueryBlockingCallback</b> function returns a pointer to a callback function the service provider should invoke periodically while servicing blocking operations.


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
<b>WPUQueryBlockingCallback</b> returns zero and stores a pointer to a blocking callback function in <i>lpfnCallback</i> and an associated context value in <i>lpdwContext</i>. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpfnCallback</i> or the <i>lpdwContext</i> parameter is not a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
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
<b>WPUQueryBlockingCallback</b> function returns a pointer to a callback function in <i>lpfnCallback</i> to be invoked periodically during blocking operations. This function also returns a context value in <i>lpdwContext</i> to be passed into the blocking callback.

In Windows, this function can return null in <i>lpfnCallback</i>, indicating that no user defined–blocking hook is installed. In this case, the service provider should use the native Windows synchronization objects to implement blocking.

LPBLOCKINGCALLBACK is defined as follows:


```cpp
typedef BOOL ( CALLBACK FAR * LPBLOCKINGCALLBACK )( DWORD dwContext );

```


The blocking callback will return <b>TRUE</b> if the service provider is to continue waiting for the blocking operation to complete. It will return <b>FALSE</b> if the blocking operation has been canceled with the 
<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>.

Any missing components of the address will default to a reasonable value if possible. For example, a missing port number will default to zero.




## -see-also




<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>
 

 

