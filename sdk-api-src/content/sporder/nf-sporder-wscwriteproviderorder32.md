---
UID: NF:sporder.WSCWriteProviderOrder32
title: WSCWriteProviderOrder32 function
author: windows-sdk-content
description: Used to reorder the available 32-bit transport providers.
old-location: winsock\wscwriteproviderorder32.htm
tech.root: winsock
ms.assetid: 03ce09b4-d80e-480d-9219-d226df055f18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSCWriteProviderOrder32, WSCWriteProviderOrder32 function [Winsock], sporder/WSCWriteProviderOrder32, winsock.wscwriteproviderorder32
ms.topic: function
req.header: sporder.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 x64 Edition [desktop apps only]
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
 - WSCWriteProviderOrder32
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSCWriteProviderOrder32 function


## -description


The 
<b>WSCWriteProviderOrder32</b> function is used to reorder the available 32-bit transport providers. The order of the protocols determines the priority of a protocol when being enumerated or selected for use.
<div class="alert"><b>Note</b>  This call is a strictly 32-bit version of <a href="https://msdn.microsoft.com/459a2fc9-fa05-4ebc-8cc7-3f4915b4b800">WSCWriteProviderOrder</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to modify the 32-bit catalogs.</div><div> </div>

## -parameters




### -param lpwdCatalogEntryId [in]

A pointer to an array of <b>CatalogEntryId</b> elements found in the 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure. The order of the <b>CatalogEntryId</b> elements is the new priority ordering for the protocols.


### -param dwNumberOfEntries [in]

The number of elements in the <i>lpwdCatalogEntryId</i> array.


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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid, no action was taken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the  Winsock registry, or a failure occurred when opening or writing a catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>(other)</b></dt>
</dl>
</td>
<td width="60%">
The routine may return any registry error code.

</td>
</tr>
</table>
 




## -remarks



The <b>WSCWriteProviderOrder32</b> function is a strictly 32-bit version of the <a href="https://msdn.microsoft.com/459a2fc9-fa05-4ebc-8cc7-3f4915b4b800">WSCWriteProviderOrder</a> function. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The order in which transport service providers are initially installed governs the order in which they are enumerated through 
<a href="https://msdn.microsoft.com/f46042f6-0b14-4a14-abc1-4e40c34b1599">WSCEnumProtocols32</a> at the service provider interface, or through 
<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a> at the application interface. More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.

Windows Sockets 2 includes an application called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed. Windows Sockets 2 also includes an auxiliary DLL, <i>Sporder.dll</i> that exports this procedural interface for reordering protocols. This interface can be imported by linking with <i>Sporder.lib</i>.


The following are scenarios in which the 
<b>WSCWriteProviderOrder32</b> function could fail:

<ul>
<li>The <i>dwNumberOfEntries</i> parameter is not equal to the number of registered service providers.</li>
<li>The <i>lpwdCatalogEntryId</i> contains an invalid catalog identifier.</li>
<li>The <i>lpwdCatalogEntryId</i> does not contain all valid catalog identifiers exactly one time.</li>
<li>The routine is not able to access the registry for some reason (for example, inadequate user permissions).</li>
<li>Another process (or thread) is currently calling the function.</li>
</ul>


On success, <b>WSCWriteProviderOrder32</b> will attempt to alert all interested applications that have registered for notification of the change by calling <a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>.

The <b>WSCWriteProviderOrder32</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCWriteProviderOrder32</b> is called by a user that is not a member of the Administrators group, the function call will fail and 
								<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a> is returned. 
 For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (<b>RunAs administrator</b>) for this function to succeed.




## -see-also




<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a>



<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a>



<a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>



<a href="https://msdn.microsoft.com/f46042f6-0b14-4a14-abc1-4e40c34b1599">WSCEnumProtocols32</a>
 

 

