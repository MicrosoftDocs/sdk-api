---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpfnCallback</i> or the <i>lpdwContext</i> parameter is not a valid part of the process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef BOOL ( CALLBACK FAR * LPBLOCKINGCALLBACK )( DWORD dwContext );
</pre>
</td>
</tr>
</table></span></div>
The blocking callback will return <b>TRUE</b> if the service provider is to continue waiting for the blocking operation to complete. It will return <b>FALSE</b> if the blocking operation has been canceled with the 
<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>.

Any missing components of the address will default to a reasonable value if possible. For example, a missing port number will default to zero.




## -see-also




<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>
 

 

