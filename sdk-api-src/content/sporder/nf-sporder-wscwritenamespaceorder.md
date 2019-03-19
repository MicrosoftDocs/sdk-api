---
UID: NF:sporder.WSCWriteNameSpaceOrder
title: WSCWriteNameSpaceOrder function (sporder.h)
author: windows-sdk-content
description: Changes the order of available Windows Sockets (Winsock) 2 namespace providers. The order of the namespace providers determines the priority of the namespace when enumerated or queried for name resolution.
old-location: winsock\wscwritenamespaceorder.htm
tech.root: WinSock
ms.assetid: 00a06104-570f-4cd5-9520-bc73516ac7a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSCWriteNameSpaceOrder, WSCWriteNameSpaceOrder function [Winsock], sporder/WSCWriteNameSpaceOrder, winsock.wscwritenamespaceorder
ms.topic: function
req.header: sporder.h
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
req.lib: Sporder.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSCWriteNameSpaceOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSCWriteNameSpaceOrder function


## -description


The 
<b>WSCWriteNameSpaceOrder</b> function changes the order of available Windows Sockets (Winsock) 2 namespace providers. The order of the namespace providers determines the priority of the namespace when enumerated or queried for name resolution.


## -parameters




### -param lpProviderId [in]

An array of <b>NSProviderId</b> elements as found in the <a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFO</a>structure.  The order of the <b>NSProviderId</b> elements is the new
      priority ordering for the namespace providers.


### -param dwNumberOfEntries [in]

The number of elements in the <b>NSProviderId</b> array.


## -returns



The function returns <b>ERROR_SUCCESS</b> (zero) if the routine is successful. Otherwise, it returns a specific error code.

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
The <b>NSProviderId</b> array is not fully contained within process address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments are input parameters were invalid, no action was taken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the  Winsock registry or another application is currently writing to the namespace provider catalog.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSASYSCALLFAILURE</a></b></dt>
</dl>
</td>
<td width="60%">
A system call that should never fail has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx"> WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
The function is called by another thread or process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory was available to perform the operation. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>(other)</b></dt>
</dl>
</td>
<td width="60%">
The function may return any registry error code.

</td>
</tr>
</table>
 




## -remarks



Namespace providers are installed using the <a href="https://msdn.microsoft.com/f17f6174-879e-45e7-a250-975d1ee24fe0">WSCInstallNameSpace</a> function. The order in which namespace providers are initially installed governs the default order in which they are enumerated through 
 <a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>.  More importantly, this order also governs the order in which namespace providers are considered when a client requests name resolution. The order of namespace providers can be changed using the <b>WSCWriteNameSpaceOrder</b> function. On 64-bit platforms, the <a href="https://msdn.microsoft.com/a5b15d28-8137-42bf-8f2a-7c6b5a8a63c2">WSCWriteNameSpaceOrder32</a> function is provided to allow 64-bit processes to change the order of namespace providers in the 32-bit namespace provider catalog. On 64-bit platforms, namespace providers are installed in the 32-bit namespace provider catalog using the <a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a> function. 

The current namespace provider catalog is stored in the registry under the following registry key: <b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>Current Control Set</b>\<b>Services</b>\<b>Winsock2</b>\<b>Parameters</b>\<b>NameSpace_Catalog5</b>



A client request for name resolution uses the <a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>, <a href="https://msdn.microsoft.com/ab4f1830-b38d-4224-a6a9-6d4512245ad6">WSALookupServiceNext</a>, and <a href="https://msdn.microsoft.com/f9d2ac54-a818-464d-918e-80ebb5b1b106">WSALookupServiceEnd</a> routines. The <b>dwNameSpace</b> member of the <a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> structure passed to <b>WSALookupServiceBegin</b> is set to the identifier of a single namespace (NS_DNS, for example) in which to constrain the search, or <b>NS_ALL</b> to include all namespaces. If multiple namespace providers support a specific namespace (<b>NS_DNS</b>, for example), then the results from all namespace providers that match the requested <b>dwNameSpace</b> are returned unless the <b>lpNSProviderId</b> 
member is set to a specific namespace provider. The results from all namespace providers is returned if NS_ALL is specified for the <b>dwNameSpace</b> member. The order that the results are returned is dependent on the namespace provider order in the catalog.  

The Windows SDK includes an application called SpOrder.exe that allows the catalog of installed namespace providers to be displayed. Windows Sockets 2 includes the ws2_32.dll that exports the  <b>WSCWriteNameSpaceOrder</b> function for reordering namespace providers in the catalog. This interface can be imported by linking with WS2_32.lib. For computers running on Windows XP with Service Pack 2 (SP2) and Windows Server 2003 with Service Pack 1 (SP1) and later, the <b>netsh.exe winsock show catalog</b> command will display both the protocol and namespace providers installed on the system.

<b>WSCWriteNameSpaceOrder</b> can only be called by a user logged on as a member of the Administrators group. If <b>WSCWriteNameSpaceOrder</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>WSANO_RECOVERY</b> is returned in the <i>lpErrno</i> parameter.

For computers running on Windows Vista and Windows Vista, this function can also fail because of user account control (UAC). If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista and Windows Vista lacks this setting in the manifest file used to build the executable file, a user logged on as a member of the Administrators group other than the Administrator must then be executing the application in an enhanced shell as the  Administrator (<b>RunAs administrator</b>) for this function to succeed.

The following list describes scenarios in which the 
<b>WSCWriteNameSpaceOrder</b> function could fail:

<ul>
<li>The <i>dwNumberOfEntries</i> parameter is not equal to the number of registered namespace providers.</li>
<li>The <b>NSProviderId</b> array contains an invalid namespace provider identifier.</li>
<li>The <b>NSProviderId</b> array does not contain all valid namespace provider identifiers exactly one time.</li>
<li>The function cannot access the registry (for example, insufficient user permissions).</li>
<li>Another process (or thread) is currently calling the function.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFO</a>



<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/792737d9-231d-4524-b1a6-b9904951d5b4">WSCEnumNameSpaceProviders32</a>



<a href="https://msdn.microsoft.com/f17f6174-879e-45e7-a250-975d1ee24fe0">WSCInstallNameSpace</a>



<a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a>



<a href="https://msdn.microsoft.com/a5b15d28-8137-42bf-8f2a-7c6b5a8a63c2">WSCWriteNameSpaceOrder32</a>
 

 

